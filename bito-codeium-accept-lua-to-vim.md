Here's the generated Vimscript code:

```vim
function! Source_complete(params, callback)
  let context = a:params.context
  let offset = a:params.offset
  let cursor = context.cursor
  let bufnr = context.bufnr
  let filetype = get(enums.filetype_aliases, context.filetype, context.filetype)
  let language = get(enums.languages, filetype, enums.languages.unspecified)
  let after_line = context.cursor_after_line
  let before_line = context.cursor_before_line
  let line_ending = util.get_newline(bufnr)
  let line_ending_len = len(line_ending)
  let editor_options = util.get_editor_options(bufnr)

  " We need to calculate the number of bytes prior to the current character, that starts with all the prior lines
  let lines = nvim_buf_get_lines(bufnr, 0, -1, v:true)

  " For the current line, we want to exclude any extra characters that were entered after the popup displayed
  let lines[cursor.row] = context.cursor_line

  " We exclude the current line from the loop below, so add its length here
  let cursor_offset = len(before_line)
  for i in range(1, cursor.row - 1)
    let line = lines[i]
    let cursor_offset += len(line) + line_ending_len
  endfor

  " Ensure that there is always a newline at the end of the file
  call add(lines, "")

  let text = join(lines, line_ending)

  let cancel
  let remove_event = require("cmp").event:on("menu_closed", cancel)

  function! handle_completions(completion_items)
    let duplicates = {}
    let completions = []
    for comp in a:completion_items
      if !has_key(duplicates, comp.completion.text)
        let duplicates[comp.completion.text] = v:true
        call add(completions, codeium_to_cmp(comp, offset, after_line))
      endif
    endfor
    call callback(completions)
  endfunction

  let cancel = self.server.request_completion({
        \ "editor_language": filetype,
        \ "language": language,
        \ "cursor_offset": cursor_offset,
        \ "text": text,
        \ "line_ending": line_ending,
        \ }, editor_options,
        \ function(success, json)
        \   call remove_event()
        \   if !success
        \     call callback([])
        \   endif
        \   if json && json.state && json.state.state == "CODEIUM_STATE_SUCCESS" && json.completionItems
        \     call handle_completions(json.completionItems)
        \   else
        \     call callback([])
        \   endif
        \ endfunction)
endfunction
```

Please note that the generated code may require further modification and testing to ensure it works as expected in your specific Vimscript environment.


