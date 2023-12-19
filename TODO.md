# codeium.nvim

## TODO

- [ ] manually trigger codeium accept function similar to codeium.vim
- [ ] manually trigger codeium accept function on cmp menu selection confirmation



```lua
-- print(vim.inspect(cmp.get_entries()))

for _, entry in ipairs(cmp.get_entries()) do
  if entry.source.name == "codeium" then
    print(vim.inspect(entry.source.name))
    -- print(vim.inspect(entry.source.entries))

    -- NOTE: `entry:get_completion_item().label` is equivalent to the left-hand side of the cmp pmenu
    print(vim.inspect(entry:get_completion_item().label))
  end
end
```


```lua
--- `lua vim.print(vim.inspect(require("cmp")))`
{
  ConfirmBehavior = {
    Insert = "insert",
    Replace = "replace"
  },
  ContextReason = {
    Auto = "auto",
    Manual = "manual",
    None = "none",
    TriggerOnly = "triggerOnly"
  },
  ItemField = {
    Abbr = "abbr",
    Kind = "kind",
    Menu = "menu"
  },
  PreselectMode = {
    Item = "item",
    None = "none"
  },
  SelectBehavior = {
    Insert = "insert",
    Select = "select"
  },
  TriggerEvent = {
    InsertEnter = "InsertEnter",
    TextChanged = "TextChanged"
  },
  abort = <function 1>,
  close = <function 2>,
  close_docs = <function 3>,
  complete = <function 4>,
  complete_common_string = <function 5>,
  config = {
    compare = {
      exact = <function 6>,
      kind = <function 7>,
      length = <function 8>,
      locality = {
        lines_cache = {
          entries = {
            buf = 9,
            ["line:"] = {},
            ["line:\tlocal after_line = context.cursor_after_line"] = {
              after_line = 7,
              context = 7,
              cursor_after_line = 7,
              ["local"] = 7
            },
            ["line:\tlocal before_line = context.cursor_before_line"] = {
              before_line = 8,
              context = 8,
              cursor_before_line = 8,
              ["local"] = 8
            },
            ["line:\tlocal bufnr = context.bufnr"] = {
              bufnr = 4,
              context = 4,
              ["local"] = 4
            },
            ["line:\tlocal context = params.context"] = {
              context = 1,
              ["local"] = 1,
              params = 1
            },
            ["line:\tlocal cursor = context.cursor"] = {
              context = 3,
              cursor = 3,
              ["local"] = 3
            },
            ['line:\tlocal filetype = enums.filetype_aliases[context.filetype] or context.filetype or "text"'] = {
              context = 5,
              enums = 5,
              filetype = 5,
              filetype_aliases = 5,
              ["local"] = 5,
              ["or"] = 5,
              text = 5
            },
            ["line:\tlocal language = enums.languages[filetype] or enums.languages.unspecified"] = {
              enums = 6,
              filetype = 6,
              language = 6,
              languages = 6,
              ["local"] = 6,
              ["or"] = 6,
              unspecified = 6
            },
            ["line:\tlocal line_ending = util.get_newline(bufnr)"] = {
              bufnr = 9,
              get_newline = 9,
              line_ending = 9,
              ["local"] = 9,
              util = 9
            },
            ["line:\tlocal line_ending_len = utf8len(line_ending)"] = {
              line_ending = 10,
              line_ending_len = 10,
              ["local"] = 10,
              utf8len = 10
            },
            ["line:\tlocal offset = params.offset"] = {
              ["local"] = 2,
              offset = 2,
              params = 2
            },
            ["line:\to.server = server"] = {
              o = 9,
              server = 9
            },
            ['line:\treturn "utf-8"'] = {
              ["return"] = 2,
              ["utf-8"] = 2
            },
            ["line:\treturn o"] = {
              o = 9,
              ["return"] = 9
            },
            ["line:\treturn self.server.is_healthy()"] = {
              is_healthy = 6,
              ["return"] = 6,
              self = 6,
              server = 6
            },
            ["line:end"] = {
              ["end"] = 9
            },
            ["line:function Source:complete(params, callback)"] = {
              Source = 0,
              callback = 0,
              complete = 0,
              ["function"] = 0,
              params = 0
            },
            ["line:function Source:get_position_encoding_kind()"] = {
              Source = 3,
              ["function"] = 3,
              get_position_encoding_kind = 3
            },
            ["line:function Source:highlight()"] = {
              Source = 0,
              ["function"] = 0,
              highlight = 0
            },
            ["line:function Source:is_available()"] = {
              Source = 7,
              ["function"] = 7,
              is_available = 7
            }
          },
          <metatable> = {
            __index = <1>{
              clear = <function 9>,
              ensure = <function 10>,
              get = <function 11>,
              key = <function 12>,
              new = <function 13>,
              set = <function 14>
            }
          }
        },
        lines_count = 10,
        locality_map = {
          Source = 2,
          after_line = 7,
          before_line = 8,
          bufnr = 4,
          callback = 0,
          complete = 0,
          context = 1,
          cursor = 3,
          cursor_after_line = 7,
          cursor_before_line = 8,
          ["end"] = 0,
          enums = 5,
          filetype = 5,
          filetype_aliases = 5,
          ["function"] = 2,
          get_position_encoding_kind = 2,
          is_available = 6,
          is_healthy = 5,
          language = 6,
          languages = 6,
          ["local"] = 1,
          o = 9,
          offset = 2,
          ["or"] = 5,
          params = 0,
          ["return"] = 1,
          self = 5,
          server = 5,
          text = 5,
          unspecified = 6,
          ["utf-8"] = 1
        },
        update = <function 15>,
        <metatable> = {
          __call = <function 16>
        }
      },
      offset = <function 17>,
      order = <function 18>,
      recently_used = {
        add_entry = <function 19>,
        records = {
          BitoAiGenerate = 125885768,
          ["function Source:highlight()\nend"] = 126164898
        },
        <metatable> = {
          __call = <function 20>
        }
      },
      scopes = {
        scopes_map = {},
        update = <function 21>,
        <metatable> = {
          __call = <function 22>
        }
      },
      score = <function 23>,
      sort_text = <function 24>
    },
    disable = vim.NIL,
    mapping = <2>{
      abort = <function 25>,
      close = <function 26>,
      close_docs = <function 27>,
      complete = <function 28>,
      complete_common_string = <function 29>,
      confirm = <function 30>,
      open_docs = <function 31>,
      preset = {
        cmdline = <function 32>,
        insert = <function 33>
      },
      scroll_docs = <function 34>,
      select_next_item = <function 35>,
      select_prev_item = <function 36>,
      <metatable> = {
        __call = <function 37>
      }
    },
    sources = <function 38>,
    window = {
      bordered = <function 39>
    }
  },
  confirm = <function 40>,
  core = {
    context = {
      aborted = false,
      bufnr = -1,
      cache = {
        entries = {},
        <metatable> = {
          __index = <table 1>
        }
      },
      cursor = {
        col = -1,
        row = -1
      },
      cursor_after_line = '")))',
      cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
      cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
      filetype = "lua",
      id = 5781,
      input = "",
      option = {},
      prev_context = {},
      time = 126199957,
      <metatable> = {
        __index = <3>{
          abort = <function 41>,
          changed = <function 42>,
          clone = <function 43>,
          empty = <function 44>,
          get_offset = <function 45>,
          get_reason = <function 46>,
          new = <function 47>
        }
      }
    },
    event = <4>{
      events = {
        complete_done = { <function 48> },
        confirm_done = { <function 49> },
        menu_closed = {}
      },
      <metatable> = {
        __index = <5>{
          clear = <function 50>,
          emit = <function 51>,
          new = <function 52>,
          off = <function 53>,
          on = <function 54>
        }
      }
    },
    sources = { {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 55>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5768,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 1,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "nvim_lua",
        offset = -1,
        request_offset = -1,
        revision = 455,
        source = {
          regex = <userdata 1>,
          <metatable> = {
            __index = {
              complete = <function 56>,
              get_keyword_pattern = <function 57>,
              get_trigger_characters = <function 58>,
              is_available = <function 59>,
              item = <function 60>,
              items = <function 61>,
              new = <function 62>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <6>{
            SourceStatus = {
              COMPLETED = 3,
              FETCHING = 2,
              WAITING = 1
            },
            complete = <function 63>,
            execute = <function 64>,
            get_debug_name = <function 65>,
            get_default_insert_range = <function 66>,
            get_default_replace_range = <function 67>,
            get_entries = <function 68>,
            get_entry_filter = <function 69>,
            get_fetching_time = <function 70>,
            get_keyword_length = <function 71>,
            get_keyword_pattern = <function 72>,
            get_matching_config = <function 73>,
            get_position_encoding_kind = <function 74>,
            get_source_config = <function 75>,
            get_trigger_characters = <function 76>,
            is_available = <function 77>,
            new = <function 78>,
            reset = <function 79>,
            resolve = <function 80>
          }
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 81>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5769,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 2,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "async_path",
        offset = -1,
        request_offset = -1,
        revision = 461,
        source = {
          <metatable> = {
            __index = {
              _candidates = <function 82>,
              _dirname = <function 83>,
              _get_documentation = <function 84>,
              _is_slash_comment = <function 85>,
              _validate_option = <function 86>,
              complete = <function 87>,
              get_keyword_pattern = <function 88>,
              get_trigger_characters = <function 89>,
              new = <function 90>,
              resolve = <function 91>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 92>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5770,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 3,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "buffer",
        offset = -1,
        request_offset = -1,
        revision = 457,
        source = {
          buffers = {
            [9] = {
              bufnr = 9,
              closed = false,
              last_edit_first_line = 93,
              last_edit_last_line = 93,
              lines_count = 167,
              lines_words = { { "local", "enums", "require", "codeium", "enums" }, { "local", "util", "require", "codeium", "util" }, {}, { "local", "function", "utf8len", "str" }, { "if", "str", "or", "not", "str", "then" }, { "return", "0" }, { "end" }, { "--", "TODO", "Figure", "out", "how", "to", "convert", "the", "document", "encoding", "to", "UTF8", "length" }, { "--", "Bonus", "points", "for", "doing", "it", "with", "raw", "codepoints", "instead", "of", "converting", "the" }, { "--", "string", "wholesale" }, { "return", "string", "len", "str" }, { "end" }, {}, { "local", "function", "codeium_to_cmp", "comp", "offset", "right" }, { "local", "documentation", "comp", "completion", "text" }, {}, { "local", "label", "string", "sub", "documentation", "offset" }, { "if", "string", "sub", "label", "-", "#right", "right", "then" }, { "label", "string", "sub", "label", "1", "-", "#right", "-", "1" }, { "end" }, {}, { "--", "We", "get", "the", "completion", "part", "that", "has", "the", "largest", "offset" }, { "local", "max_offset", "offset" }, { "if", "comp", "completionParts", "then" }, { "for", "_", "v", "in", "pairs", "comp", "completionParts", "do" }, { "local", "part_offset", "tonumber", "v", "offset" }, { "if", "part_offset", "max_offset", "then" }, { "max_offset", "part_offset" }, { "end" }, { "end" }, { "end" }, {}, { "--", "We", "get", "where", "the", "suffix", "difference", "between", "the", "completion", "and", "the", "range", "of", "code" }, { "local", "suffix_diff", "comp", "range", "endOffset", "-", "max_offset" }, {}, { "local", "range" }, { "start" }, { "--", "Codeium", "returns", "an", "empty", "row", "for", "the", "first", "line" }, { "line", "tonumber", "comp", "range", "startPosition", "row", "or", "0" }, { "character", "offset", "-", "1" }, {}, { "end" }, { "--", "Codeium", "returns", "an", "empty", "row", "for", "the", "first", "line" }, { "line", "tonumber", "comp", "range", "endPosition", "row", "or", "0" }, { "--", "We", "only", "want", "to", "replace", "up", "to", "where", "the", "completion", "ends" }, { "character", "comp", "range", "endPosition", "col", "or", "suffix_diff", "-", "suffix_diff" }, {}, {}, {}, { "return" }, { "type", "1" }, { "documentation" }, { "kind", "markdown" }, { "value", "table", "concat" }, { "vim", "api", "nvim_buf_get_option", "0", "filetype" }, { "label" }, {}, { "n" }, {}, { "label", "label" }, { "insertText", "label" }, { "textEdit" }, { "newText", "label" }, { "insert", "range" }, { "replace", "range" }, {}, { "cmp" }, { "kind_text", "Codeium" }, { "kind_hl_group", "CmpItemKindCodeium" }, {}, {}, { "end" }, {}, { "local", "Source" }, { "server", "nil" }, {}, { "Source", "__index", "Source" }, {}, { "function", "Source", "new", "server" }, { "local", "o" }, { "setmetatable", "o", "self" }, {}, { "o", "server", "server" }, { "return", "o" }, { "end" }, {}, { "function", "Source", "is_available" }, { "return", "self", "server", "is_healthy" }, { "end" }, {}, { "function", "Source", "get_position_encoding_kind" }, { "return", "utf-8" }, { "end" }, {}, { "function", "Source", "complete", "params", "callback" }, { "local", "context", "params", "context" }, { "local", "offset", "params", "offset" }, { "local", "cursor", "context", "cursor" }, { "local", "bufnr", "context", "bufnr" }, { "local", "filetype", "enums", "filetype_aliases", "context", "filetype", "or", "context", "filetype", "or", "text" }, { "local", "language", "enums", "languages", "filetype", "or", "enums", "languages", "unspecified" }, { "local", "after_line", "context", "cursor_after_line" }, { "local", "before_line", "context", "cursor_before_line" }, { "local", "line_ending", "util", "get_newline", "bufnr" }, { "local", "line_ending_len", "utf8len", "line_ending" }, { "local", "editor_options", "util", "get_editor_options", "bufnr" }, {}, { "--", "We", "need", "to", "calculate", "the", "number", "of", "bytes", "prior", "to", "the", "current", "character" }, { "--", "that", "starts", "with", "all", "the", "prior", "lines" }, { "local", "lines", "vim", "api", "nvim_buf_get_lines", "bufnr", "0", "-1", "true" }, {}, { "--", "For", "the", "current", "line", "we", "want", "to", "exclude", "any", "extra", "characters", "that", "were" }, { "--", "entered", "after", "the", "popup", "displayed" }, { "lines", "cursor", "row", "context", "cursor_line" }, {}, { "--", "We", "exclude", "the", "current", "line", "from", "the", "loop", "below", "so", "add", "it", "s", "length", "here" }, { "local", "cursor_offset", "utf8len", "before_line" }, { "for", "i", "1", "cursor", "row", "-", "1", "do" }, { "local", "line", "lines", "i" }, { "cursor_offset", "cursor_offset", "utf8len", "line", "line_ending_len" }, { "end" }, {}, { "--", "Ensure", "that", "there", "is", "always", "a", "newline", "at", "the", "end", "of", "the", "file" }, { "table", "insert", "lines" }, { "local", "text", "table", "concat", "lines", "line_ending" }, {}, { "local", "cancel" }, { "local", "remove_event", "require", "cmp", "event", "on", "menu_closed", "cancel" }, {}, { "local", "function", "handle_completions", "completion_items" }, { "local", "duplicates" }, { "local", "completions" }, { "for", "_", "comp", "in", "ipairs", "completion_items", "do" }, { "if", "not", "duplicates", "comp", "completion", "text", "then" }, { "duplicates", "comp", "completion", "text", "true" }, { "table", "insert", "completions", "codeium_to_cmp", "comp", "offset", "after_line" }, { "end" }, { "end" }, { "callback", "completions" }, { "end" }, {}, { "cancel", "self", "server", "request_completion" }, {}, { "editor_language", "filetype" }, { "language", "language" }, { "cursor_offset", "cursor_offset" }, { "text", "text" }, { "line_ending", "line_ending" }, {}, { "editor_options" }, { "function", "success", "json" }, { "remove_event" }, {}, { "if", "not", "success", "then" }, { "callback", "nil" }, { "end" }, {}, { "if", "json", "and", "json", "state", "and", "json", "state", "state", "CODEIUM_STATE_SUCCESS", "and", "json", "completionItems", "then" }, { "handle_completions", "json", "completionItems" }, { "else" }, { "callback", "nil" }, { "end" }, { "end" }, {}, { "end" }, {}, { "return", "Source" } },
              on_close_cb = <function 93>,
              opts = <7>{
                get_bufnrs = <function 94>,
                indexing_batch_size = 1000,
                indexing_interval = 100,
                keyword_length = 0,
                keyword_pattern = "\\k\\+",
                max_indexed_line_length = 40960
              },
              regex = <userdata 2>,
              timer = {
                handle = <userdata 3>,
                <metatable> = {
                  __index = <8>{
                    close = <function 95>,
                    is_active = <function 96>,
                    new = <function 97>,
                    start = <function 98>,
                    stop = <function 99>
                  }
                }
              },
              timer_current_line = 169,
              unique_words_curr_line = {
                fu = true
              },
              unique_words_curr_line_dirty = true,
              unique_words_other_lines = {
                ["#right"] = true,
                ["-"] = true,
                ["--"] = true,
                ["-1"] = true,
                ["0"] = true,
                ["1"] = true,
                Bonus = true,
                CODEIUM_STATE_SUCCESS = true,
                CmpItemKindCodeium = true,
                Codeium = true,
                Ensure = true,
                Figure = true,
                For = true,
                Source = true,
                TODO = true,
                UTF8 = true,
                We = true,
                _ = true,
                __index = true,
                a = true,
                add = true,
                after = true,
                after_line = true,
                all = true,
                always = true,
                an = true,
                ["and"] = true,
                any = true,
                api = true,
                at = true,
                before_line = true,
                below = true,
                between = true,
                bufnr = true,
                bytes = true,
                calculate = true,
                callback = true,
                cancel = true,
                character = true,
                characters = true,
                cmp = true,
                code = true,
                codeium = true,
                codeium_to_cmp = true,
                codepoints = true,
                col = true,
                comp = true,
                complete = true,
                completion = true,
                completionItems = true,
                completionParts = true,
                completion_items = true,
                completions = true,
                concat = true,
                context = true,
                convert = true,
                converting = true,
                current = true,
                cursor = true,
                cursor_after_line = true,
                cursor_before_line = true,
                cursor_line = true,
                cursor_offset = true,
                difference = true,
                displayed = true,
                ["do"] = true,
                document = true,
                documentation = true,
                doing = true,
                duplicates = true,
                editor_language = true,
                editor_options = true,
                ["else"] = true,
                empty = true,
                encoding = true,
                ["end"] = true,
                endOffset = true,
                endPosition = true,
                ends = true,
                entered = true,
                enums = true,
                event = true,
                exclude = true,
                extra = true,
                file = true,
                filetype = true,
                filetype_aliases = true,
                first = true,
                ["for"] = true,
                from = true,
                ["function"] = true,
                get = true,
                get_editor_options = true,
                get_newline = true,
                get_position_encoding_kind = true,
                handle_completions = true,
                has = true,
                here = true,
                how = true,
                i = true,
                ["if"] = true,
                ["in"] = true,
                insert = true,
                insertText = true,
                instead = true,
                ipairs = true,
                is = true,
                is_available = true,
                is_healthy = true,
                it = true,
                json = true,
                kind = true,
                kind_hl_group = true,
                kind_text = true,
                label = true,
                language = true,
                languages = true,
                largest = true,
                len = true,
                length = true,
                line = true,
                line_ending = true,
                line_ending_len = true,
                lines = true,
                ["local"] = true,
                loop = true,
                markdown = true,
                max_offset = true,
                menu_closed = true,
                n = true,
                need = true,
                new = true,
                newText = true,
                newline = true,
                ["nil"] = true,
                ["not"] = true,
                number = true,
                nvim_buf_get_lines = true,
                nvim_buf_get_option = true,
                o = true,
                of = true,
                offset = true,
                on = true,
                only = true,
                ["or"] = true,
                out = true,
                pairs = true,
                params = true,
                part = true,
                part_offset = true,
                points = true,
                popup = true,
                prior = true,
                range = true,
                raw = true,
                remove_event = true,
                replace = true,
                request_completion = true,
                require = true,
                ["return"] = true,
                returns = true,
                right = true,
                row = true,
                s = true,
                self = true,
                server = true,
                setmetatable = true,
                so = true,
                start = true,
                startPosition = true,
                starts = true,
                state = true,
                str = true,
                string = true,
                sub = true,
                success = true,
                suffix = true,
                suffix_diff = true,
                table = true,
                text = true,
                textEdit = true,
                that = true,
                the = true,
                ["then"] = true,
                there = true,
                to = true,
                tonumber = true,
                ["true"] = true,
                type = true,
                unspecified = true,
                up = true,
                ["utf-8"] = true,
                utf8len = true,
                util = true,
                v = true,
                value = true,
                vim = true,
                want = true,
                we = true,
                were = true,
                where = true,
                wholesale = true,
                with = true
              },
              unique_words_other_lines_dirty = true,
              words_distances = {},
              words_distances_dirty = true,
              words_distances_last_cursor_row = 0,
              <metatable> = {
                __index = <9>{
                  GET_LINES_CHUNK_SIZE = 1000,
                  close = <function 100>,
                  get_words = <function 101>,
                  get_words_distances = <function 102>,
                  index_line = <function 103>,
                  index_range = <function 104>,
                  mark_all_lines_dirty = <function 105>,
                  new = <function 106>,
                  rebuild_unique_words = <function 107>,
                  safe_buf_call = <function 108>,
                  start_indexing_timer = <function 109>,
                  stop_indexing_timer = <function 110>,
                  watch = <function 111>
                }
              }
            },
            [190] = {
              bufnr = 190,
              closed = false,
              last_edit_first_line = 0,
              last_edit_last_line = 0,
              lines_count = 73,
              lines_words = { { "Here", "s", "the", "generated", "Vimscript", "code" }, {}, { "vim" }, { "function", "Source_complete", "params", "callback" }, { "let", "context", "a", "params", "context" }, { "let", "offset", "a", "params", "offset" }, { "let", "cursor", "context", "cursor" }, { "let", "bufnr", "context", "bufnr" }, { "let", "filetype", "get", "enums", "filetype_aliases", "context", "filetype", "context", "filetype" }, { "let", "language", "get", "enums", "languages", "filetype", "enums", "languages", "unspecified" }, { "let", "after_line", "context", "cursor_after_line" }, { "let", "before_line", "context", "cursor_before_line" }, { "let", "line_ending", "util", "get_newline", "bufnr" }, { "let", "line_ending_len", "len", "line_ending" }, { "let", "editor_options", "util", "get_editor_options", "bufnr" }, {}, { "We", "need", "to", "calculate", "the", "number", "of", "bytes", "prior", "to", "the", "current", "character", "that", "starts", "with", "all", "the", "prior", "lines" }, { "let", "lines", "nvim_buf_get_lines", "bufnr", "0", "-1", "v", "true" }, {}, { "For", "the", "current", "line", "we", "want", "to", "exclude", "any", "extra", "characters", "that", "were", "entered", "after", "the", "popup", "displayed" }, { "let", "lines", "cursor", "row", "context", "cursor_line" }, {}, { "We", "exclude", "the", "current", "line", "from", "the", "loop", "below", "so", "add", "its", "length", "here" }, { "let", "cursor_offset", "len", "before_line" }, { "for", "i", "in", "range", "1", "cursor", "row", "-", "1" }, { "let", "line", "lines", "i" }, { "let", "cursor_offset", "len", "line", "line_ending_len" }, { "endfor" }, {}, { "Ensure", "that", "there", "is", "always", "a", "newline", "at", "the", "end", "of", "the", "file" }, { "call", "add", "lines" }, {}, { "let", "text", "join", "lines", "line_ending" }, {}, { "let", "cancel" }, { "let", "remove_event", "require", "cmp", "event", "on", "menu_closed", "cancel" }, {}, { "function", "handle_completions", "completion_items" }, { "let", "duplicates" }, { "let", "completions" }, { "for", "comp", "in", "a", "completion_items" }, { "if", "has_key", "duplicates", "comp", "completion", "text" }, { "let", "duplicates", "comp", "completion", "text", "v", "true" }, { "call", "add", "completions", "codeium_to_cmp", "comp", "offset", "after_line" }, { "endif" }, { "endfor" }, { "call", "callback", "completions" }, { "endfunction" }, {}, { "let", "cancel", "self", "server", "request_completion" }, { "editor_language", "filetype" }, { "language", "language" }, { "cursor_offset", "cursor_offset" }, { "text", "text" }, { "line_ending", "line_ending" }, { "editor_options" }, { "function", "success", "json" }, { "call", "remove_event" }, { "if", "success" }, { "call", "callback" }, { "endif" }, { "if", "json", "json", "state", "json", "state", "state", "CODEIUM_STATE_SUCCESS", "json", "completionItems" }, { "call", "handle_completions", "json", "completionItems" }, { "else" }, { "call", "callback" }, { "endif" }, { "endfunction" }, { "endfunction" }, {}, {}, { "Please", "note", "that", "the", "generated", "code", "may", "require", "further", "modification", "and", "testing", "to", "ensure", "it", "works", "as", "expected", "in", "your", "specific", "Vimscript", "environment" }, {}, {} },
              on_close_cb = <function 112>,
              opts = <table 7>,
              regex = <userdata 4>,
              timer = {
                handle = <userdata 5>,
                <metatable> = {
                  __index = <table 8>
                }
              },
              timer_current_line = 73,
              unique_words_curr_line = {},
              unique_words_curr_line_dirty = false,
              unique_words_other_lines = {
                ["-"] = true,
                ["-1"] = true,
                ["0"] = true,
                ["1"] = true,
                CODEIUM_STATE_SUCCESS = true,
                Ensure = true,
                For = true,
                Here = true,
                Please = true,
                Source_complete = true,
                Vimscript = true,
                We = true,
                a = true,
                add = true,
                after = true,
                after_line = true,
                all = true,
                always = true,
                ["and"] = true,
                any = true,
                as = true,
                at = true,
                before_line = true,
                below = true,
                bufnr = true,
                bytes = true,
                calculate = true,
                call = true,
                callback = true,
                cancel = true,
                character = true,
                characters = true,
                cmp = true,
                code = true,
                codeium_to_cmp = true,
                comp = true,
                completion = true,
                completionItems = true,
                completion_items = true,
                completions = true,
                context = true,
                current = true,
                cursor = true,
                cursor_after_line = true,
                cursor_before_line = true,
                cursor_line = true,
                cursor_offset = true,
                displayed = true,
                duplicates = true,
                editor_language = true,
                editor_options = true,
                ["else"] = true,
                ["end"] = true,
                endfor = true,
                endfunction = true,
                endif = true,
                ensure = true,
                entered = true,
                enums = true,
                environment = true,
                event = true,
                exclude = true,
                expected = true,
                extra = true,
                file = true,
                filetype = true,
                filetype_aliases = true,
                ["for"] = true,
                from = true,
                ["function"] = true,
                further = true,
                generated = true,
                get = true,
                get_editor_options = true,
                get_newline = true,
                handle_completions = true,
                has_key = true,
                here = true,
                i = true,
                ["if"] = true,
                ["in"] = true,
                is = true,
                it = true,
                its = true,
                join = true,
                json = true,
                language = true,
                languages = true,
                len = true,
                length = true,
                let = true,
                line = true,
                line_ending = true,
                line_ending_len = true,
                lines = true,
                loop = true,
                may = true,
                menu_closed = true,
                modification = true,
                need = true,
                newline = true,
                note = true,
                number = true,
                nvim_buf_get_lines = true,
                of = true,
                offset = true,
                on = true,
                params = true,
                popup = true,
                prior = true,
                range = true,
                remove_event = true,
                request_completion = true,
                require = true,
                row = true,
                s = true,
                self = true,
                server = true,
                so = true,
                specific = true,
                starts = true,
                state = true,
                success = true,
                testing = true,
                text = true,
                that = true,
                the = true,
                there = true,
                to = true,
                ["true"] = true,
                unspecified = true,
                util = true,
                v = true,
                vim = true,
                want = true,
                we = true,
                were = true,
                with = true,
                works = true,
                your = true
              },
              unique_words_other_lines_dirty = false,
              words_distances = {},
              words_distances_dirty = true,
              words_distances_last_cursor_row = 0,
              <metatable> = {
                __index = <table 9>
              }
            },
            [201] = {
              bufnr = 201,
              closed = false,
              last_edit_first_line = 0,
              last_edit_last_line = 0,
              lines_count = 45,
              lines_words = { {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {} },
              on_close_cb = <function 113>,
              opts = <table 7>,
              regex = <userdata 6>,
              timer = {
                handle = <userdata 7>,
                <metatable> = {
                  __index = <table 8>
                }
              },
              timer_current_line = 45,
              unique_words_curr_line = {},
              unique_words_curr_line_dirty = false,
              unique_words_other_lines = {},
              unique_words_other_lines_dirty = false,
              words_distances = {},
              words_distances_dirty = true,
              words_distances_last_cursor_row = 0,
              <metatable> = {
                __index = <table 9>
              }
            }
          },
          <metatable> = {
            __index = {
              _get_buffers = <function 114>,
              _get_distance_from_entry = <function 115>,
              _validate_options = <function 116>,
              compare_locality = <function 117>,
              complete = <function 118>,
              get_keyword_pattern = <function 119>,
              new = <function 120>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 121>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5771,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 4,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "cmdline",
        offset = -1,
        request_offset = -1,
        revision = 472,
        source = {
          before_line = 'lua vim.print(vim.inspect(require("cmp',
          ctype = "cmdline",
          items = {},
          offset = 4,
          <metatable> = {
            __index = {
              complete = <function 122>,
              get_keyword_pattern = <function 123>,
              get_trigger_characters = <function 124>,
              new = <function 125>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 126>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5772,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 5,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "env",
        offset = -1,
        request_offset = -1,
        revision = 457,
        source = {
          <metatable> = {
            __index = {
              complete = <function 127>,
              get_keyword_pattern = <function 128>,
              new = <function 129>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 130>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5773,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 6,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "dynamic",
        offset = -1,
        request_offset = -1,
        revision = 456,
        source = {
          <metatable> = {
            __index = {
              _items = { {
                  insertText = <function 131>,
                  label = "today"
                }, {
                  insertText = <function 132>,
                  label = "next Monday",
                  resolve = true
                } },
              complete = <function 133>,
              get_debug_name = <function 134>,
              new = <function 135>,
              register = <function 136>,
              resolve = <function 137>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 138>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5774,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 7,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "spell",
        offset = -1,
        request_offset = -1,
        revision = 457,
        source = {
          <metatable> = {
            __index = {
              complete = <function 139>,
              get_debug_name = <function 140>,
              get_keyword_pattern = <function 141>,
              is_available = <function 142>,
              new = <function 143>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 144>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5775,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 8,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "rg",
        offset = -1,
        request_offset = -1,
        revision = 457,
        source = {
          json_decode = <function 145>,
          running_job_id = 370,
          timer = <userdata 8>,
          <metatable> = {
            __index = {
              complete = <function 146>,
              new = <function 147>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 148>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5776,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 9,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "luasnip",
        offset = -1,
        request_offset = -1,
        revision = 456,
        source = {
          <metatable> = {
            __index = {
              clear_cache = <function 149>,
              complete = <function 150>,
              execute = <function 151>,
              get_debug_name = <function 152>,
              get_keyword_pattern = <function 153>,
              is_available = <function 154>,
              new = <function 155>,
              refresh = <function 156>,
              resolve = <function 157>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 158>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5777,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 10,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "calc",
        offset = -1,
        request_offset = -1,
        revision = 456,
        source = {
          <metatable> = {
            __index = {
              _analyze = <function 159>,
              _keyptn = "\\s*\\zs\\(\\d\\+\\(\\.\\d\\+\\)\\?\\|[ ()^*/%+-]\\|pow\\|fmod\\|ldexp\\|min\\|max\\|pi\\|huge\\|random\\|randomseed\\|abs\\|floor\\|ceil\\|sqrt\\|log10\\|exp\\|sin\\|cos\\|tan\\|asin\\|acos\\|atan\\|sinh\\|cosh\\|tanh\\|frexp\\|modf\\|log\\|deg\\|rad\\|atan2\\)\\+",
              _trigger_chars = { "0", "1", "2", "3", "4", "5", "6", "7", "8", "9", ")" },
              complete = <function 160>,
              get_keyword_pattern = <function 161>,
              get_position_encoding_kind = <function 162>,
              get_trigger_characters = <function 163>,
              new = <function 164>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 165>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5778,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 11,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "codeium",
        offset = -1,
        request_offset = -1,
        revision = 456,
        source = {
          server = {
            <metatable> = <10>{
              __gc = <function 166>,
              __index = <table 10>,
              is_healthy = <function 167>,
              request_completion = <function 168>,
              shutdown = <function 169>,
              start = <function 170>,
              <metatable> = <11>{
                __index = <table 11>,
                authenticate = <function 171>,
                load_api_key = <function 172>,
                new = <function 173>,
                save_api_key = <function 174>
              }
            }
          },
          <metatable> = <12>{
            __index = <table 12>,
            complete = <function 175>,
            get_position_encoding_kind = <function 176>,
            is_available = <function 177>,
            new = <function 178>
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 179>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5779,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 12,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "nvim_lsp",
        offset = -1,
        request_offset = -1,
        revision = 9,
        source = {
          client = {
            _exec_cmd = <function 180>,
            _on_attach = <function 181>,
            attached_buffers = {
              [6] = true,
              [9] = true,
              [15] = true
            },
            cancel_request = <function 182>,
            commands = {},
            config = {
              _on_attach = <function 183>,
              autostart = true,
              capabilities = {
                general = {
                  positionEncodings = { "utf-16" }
                },
                textDocument = {
                  callHierarchy = {
                    dynamicRegistration = false
                  },
                  codeAction = {
                    codeActionLiteralSupport = {
                      codeActionKind = {
                        valueSet = { "", "quickfix", "refactor", "refactor.extract", "refactor.inline", "refactor.rewrite", "source", "source.organizeImports" }
                      }
                    },
                    dataSupport = true,
                    dynamicRegistration = false,
                    isPreferredSupport = true,
                    resolveSupport = {
                      properties = { "edit" }
                    }
                  },
                  completion = {
                    completionItem = {
                      commitCharactersSupport = true,
                      deprecatedSupport = true,
                      documentationFormat = { "markdown", "plaintext" },
                      insertReplaceSupport = true,
                      insertTextModeSupport = {
                        valueSet = { 1, 2 }
                      },
                      labelDetailsSupport = true,
                      preselectSupport = true,
                      resolveSupport = {
                        properties = { "documentation", "detail", "additionalTextEdits" }
                      },
                      snippetSupport = true,
                      tagSupport = {
                        valueSet = { 1 }
                      }
                    },
                    completionItemKind = {
                      valueSet = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25 }
                    },
                    completionList = {
                      itemDefaults = { "commitCharacters", "editRange", "insertTextFormat", "insertTextMode", "data" }
                    },
                    contextSupport = true,
                    dynamicRegistration = false,
                    insertTextMode = 1
                  },
                  declaration = {
                    linkSupport = true
                  },
                  definition = {
                    dynamicRegistration = true,
                    linkSupport = true
                  },
                  diagnostic = {
                    dynamicRegistration = false
                  },
                  documentFormattingProvider = true,
                  documentHighlight = {
                    dynamicRegistration = false
                  },
                  documentRangeFormattingProvider = true,
                  documentSymbol = {
                    dynamicRegistration = false,
                    hierarchicalDocumentSymbolSupport = true,
                    symbolKind = {
                      valueSet = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26 }
                    }
                  },
                  executeCommandProvider = true,
                  foldingRange = {
                    dynamicRegistration = false,
                    lineFoldingOnly = true
                  },
                  formatting = {
                    dynamicRegistration = true
                  },
                  hover = {
                    contentFormat = { "markdown", "plaintext" },
                    dynamicRegistration = true
                  },
                  hoverProvider = true,
                  implementation = {
                    linkSupport = true
                  },
                  inlayHint = {
                    dynamicRegistration = true,
                    resolveSupport = {
                      properties = { "textEdits", "tooltip", "location", "command" }
                    }
                  },
                  publishDiagnostics = {
                    dataSupport = true,
                    relatedInformation = true,
                    tagSupport = {
                      valueSet = { 1, 2 }
                    }
                  },
                  rangeFormatting = {
                    dynamicRegistration = true
                  },
                  references = {
                    dynamicRegistration = false
                  },
                  rename = {
                    dynamicRegistration = true,
                    prepareSupport = true
                  },
                  semanticTokens = {
                    augmentsSyntaxTokens = true,
                    dynamicRegistration = false,
                    formats = { "relative" },
                    multilineTokenSupport = false,
                    overlappingTokenSupport = true,
                    requests = {
                      full = {
                        delta = true
                      },
                      range = false
                    },
                    serverCancelSupport = false,
                    tokenModifiers = { "declaration", "definition", "readonly", "static", "deprecated", "abstract", "async", "modification", "documentation", "defaultLibrary" },
                    tokenTypes = { "namespace", "type", "class", "enum", "interface", "struct", "typeParameter", "parameter", "variable", "property", "enumMember", "event", "function", "method", "macro", "keyword", "modifier", "comment", "string", "number", "regexp", "operator", "decorator" }
                  },
                  signatureHelp = {
                    dynamicRegistration = false,
                    signatureInformation = {
                      activeParameterSupport = true,
                      documentationFormat = { "markdown", "plaintext" },
                      parameterInformation = {
                        labelOffsetSupport = true
                      }
                    }
                  },
                  synchronization = {
                    didSave = true,
                    dynamicRegistration = false,
                    willSave = true,
                    willSaveWaitUntil = true
                  },
                  textDocumentSync = {
                    change = 1,
                    openClose = true,
                    save = {
                      includeText = true
                    }
                  },
                  typeDefinition = {
                    linkSupport = true
                  }
                },
                window = {
                  showDocument = {
                    support = true
                  },
                  showMessage = {
                    messageActionItem = {
                      additionalPropertiesSupport = false
                    }
                  },
                  workDoneProgress = true
                },
                workspace = {
                  applyEdit = true,
                  configuration = true,
                  didChangeConfiguration = {
                    dynamicRegistration = false
                  },
                  didChangeWatchedFiles = {
                    dynamicRegistration = true,
                    relativePatternSupport = true
                  },
                  inlayHint = {
                    refreshSupport = true
                  },
                  semanticTokens = {
                    refreshSupport = true
                  },
                  symbol = {
                    dynamicRegistration = false,
                    symbolKind = {
                      valueSet = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26 }
                    }
                  },
                  workspaceEdit = {
                    resourceOperations = { "rename", "create", "delete" }
                  },
                  workspaceFolders = true
                }
              },
              cmd = { "/Users/chazleong/.local/share/nvim/mason/bin/lua-language-server" },
              cmd_cwd = "/Users/chazleong/my/codeium.nvim/lua/",
              filetypes = { "lua" },
              flags = {},
              get_language_id = <function 184>,
              handlers = <13>{},
              init_options = vim.empty_dict(),
              log_level = 2,
              message_level = 2,
              name = "lua_ls",
              on_attach = <function 185>,
              on_exit = <function 186>,
              on_init = <function 187>,
              on_new_config = <function 188>,
              original_settings = vim.empty_dict(),
              root_dir = "/Users/chazleong/my/codeium.nvim/lua/",
              settings = {
                Lua = {
                  addonManager = {
                    enable = true
                  },
                  codeLens = {
                    enable = true
                  },
                  completion = {
                    autoRequire = true,
                    callSnippet = "Replace",
                    displayContext = 20,
                    enable = true,
                    keywordSnippet = "Replace",
                    postfix = "@",
                    requireSeparator = ".",
                    showParams = true,
                    showWord = "Fallback",
                    workspaceWord = true
                  },
                  diagnostics = {
                    disable = { "lowercase-global", "missing-fields" },
                    disableScheme = { "git" },
                    enable = true,
                    globals = { "vim" },
                    ignoredFiles = "Opened",
                    libraryFiles = "Opened"
                  },
                  format = {
                    enable = true
                  },
                  hint = {
                    arrayIndex = "Auto",
                    await = true,
                    enable = true,
                    paramName = "All",
                    paramType = true,
                    semicolon = "SameLine",
                    setType = true
                  },
                  hover = {
                    enable = true,
                    enumsLimit = 5,
                    expandAlias = true,
                    previewFields = 50,
                    viewNumber = true,
                    viewString = true,
                    viewStringMax = 1000
                  },
                  misc = {
                    executablePath = "~/.local/share/nvim/mason/bin/lua-language-server"
                  },
                  runtime = {
                    fileEncoding = "utf8",
                    path = { "?.lua", "?/init.lua" },
                    pathStrict = true,
                    version = "LuaJIT"
                  },
                  semantic = {
                    annotation = true,
                    enable = true,
                    keyword = false,
                    variable = true
                  },
                  signatureHelp = {
                    enable = true
                  },
                  telemetry = {
                    enable = false
                  },
                  window = {
                    progressBar = true,
                    statusBar = true
                  },
                  workspace = {
                    checkThirdParty = false,
                    ignoreDir = { "types/stable", "lua", ".vscode" },
                    ignoreSubmodules = true,
                    library = { "/Users/chazleong/.local/share/nvim/lazy/neodev.nvim/types/nightly", "/opt/homebrew/Cellar/neovim/HEAD-80f75d0/share/nvim/runtime/lua", "/Users/chazleong/.local/share/nvim/lazy/neoconf.nvim/types", "/Users/chazleong/.local/share/nvim/lazy/neoconf.nvim/types/lua", "/Users/chazleong/my/codeium.nvim/lua" },
                    maxPreload = 5000,
                    preloadFileSize = 500,
                    supportScheme = { "file", "untitled", "git" },
                    useGitIgnore = true
                  }
                }
              },
              single_file_support = true,
              workspace_folders = <14>{ {
                  name = "/Users/chazleong/my/codeium.nvim/lua/",
                  uri = "file:///Users/chazleong/my/codeium.nvim/lua/"
                } },
              <metatable> = <15>{
                __tostring = <function 189>
              }
            },
            dynamic_capabilities = {
              capabilities = {},
              client_id = 2,
              <metatable> = {
                __index = <16>{
                  get = <function 190>,
                  match = <function 191>,
                  new = <function 192>,
                  register = <function 193>,
                  supports = <function 194>,
                  supports_registration = <function 195>,
                  unregister = <function 196>
                }
              }
            },
            handlers = <table 13>,
            id = 2,
            initialized = true,
            is_stopped = <function 197>,
            messages = {
              messages = {},
              name = "lua_ls",
              progress = {},
              status = {}
            },
            name = "lua_ls",
            notify = <function 198>,
            offset_encoding = "utf-16",
            progress = {
              _idx_read = 0,
              _idx_write = 24,
              _items = { {
                  token = 2,
                  value = {
                    cancellable = false,
                    kind = "begin",
                    message = "58/143",
                    percentage = 39,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3
                }, {
                  token = 3,
                  value = {
                    cancellable = false,
                    kind = "begin",
                    message = "59/131",
                    percentage = 44,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "64/143",
                    percentage = 44,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "70/131",
                    percentage = 52,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "77/143",
                    percentage = 53,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "86/131",
                    percentage = 64,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "91/131",
                    percentage = 69,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "92/143",
                    percentage = 64,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "94/131",
                    percentage = 70,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "96/143",
                    percentage = 66,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "96/131",
                    percentage = 72,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "99/143",
                    percentage = 68,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "99/131",
                    percentage = 74,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "104/143",
                    percentage = 72,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "103/131",
                    percentage = 77,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "107/143",
                    percentage = 74,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "109/131",
                    percentage = 82,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "109/143",
                    percentage = 75,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "report",
                    message = "131/131",
                    percentage = 100,
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "report",
                    message = "143/143",
                    percentage = 100,
                    title = "Loading workspace"
                  }
                }, {
                  token = 3,
                  value = {
                    kind = "end",
                    title = "Loading workspace"
                  }
                }, {
                  token = 2,
                  value = {
                    kind = "end",
                    title = "Loading workspace"
                  }
                },
                [0] = {
                  token = 2
                }
              },
              _size = 51,
              pending = {},
              <metatable> = {
                __call = <function 199>,
                __index = <17>{
                  clear = <function 200>,
                  peek = <function 201>,
                  pop = <function 202>,
                  push = <function 203>
                }
              }
            },
            request = <function 204>,
            request_sync = <function 205>,
            requests = {},
            rpc = {
              is_closing = <function 206>,
              notify = <function 207>,
              request = <function 208>,
              terminate = <function 209>
            },
            server_capabilities = {
              codeActionProvider = {
                codeActionKinds = { "", "quickfix", "refactor.rewrite", "refactor.extract" },
                resolveProvider = false
              },
              codeLensProvider = {
                resolveProvider = true
              },
              colorProvider = true,
              completionProvider = {
                resolveProvider = true,
                triggerCharacters = { "\t", "\n", ".", ":", "(", "'", '"', "[", ",", "#", "*", "@", "|", "=", "-", "{", " ", "+", "?" }
              },
              definitionProvider = true,
              documentFormattingProvider = true,
              documentHighlightProvider = true,
              documentOnTypeFormattingProvider = {
                firstTriggerCharacter = "\n"
              },
              documentRangeFormattingProvider = true,
              documentSymbolProvider = true,
              executeCommandProvider = {
                commands = { "lua.removeSpace", "lua.solve", "lua.jsonToLua", "lua.setConfig", "lua.getConfig", "lua.autoRequire" }
              },
              foldingRangeProvider = true,
              hoverProvider = true,
              inlayHintProvider = {
                resolveProvider = true
              },
              offsetEncoding = "utf-16",
              referencesProvider = true,
              renameProvider = {
                prepareProvider = true
              },
              semanticTokensProvider = {
                full = true,
                legend = {
                  tokenModifiers = { "declaration", "definition", "readonly", "static", "deprecated", "abstract", "async", "modification", "documentation", "defaultLibrary", "global" },
                  tokenTypes = { "namespace", "type", "class", "enum", "interface", "struct", "typeParameter", "parameter", "variable", "property", "enumMember", "event", "function", "method", "macro", "keyword", "modifier", "comment", "string", "number", "regexp", "operator", "decorator" }
                },
                range = true
              },
              signatureHelpProvider = {
                triggerCharacters = { "(", "," }
              },
              textDocumentSync = {
                change = 2,
                openClose = true,
                save = {
                  includeText = false
                }
              },
              typeDefinitionProvider = true,
              workspace = {
                fileOperations = {
                  didRename = {
                    filters = { {
                        pattern = {
                          glob = "/Users/chazleong/my/codeium.nvim/lua//**",
                          options = {
                            ignoreCase = true
                          }
                        }
                      } }
                  }
                },
                workspaceFolders = {
                  changeNotifications = true,
                  supported = true
                }
              },
              workspaceSymbolProvider = true
            },
            stop = <function 210>,
            supports_method = <function 211>,
            workspace_did_change_configuration = <function 212>,
            workspace_folders = <table 14>
          },
          request_ids = {},
          <metatable> = {
            __index = <18>{
              _get = <function 213>,
              _request = <function 214>,
              complete = <function 215>,
              execute = <function 216>,
              get_debug_name = <function 217>,
              get_keyword_pattern = <function 218>,
              get_position_encoding_kind = <function 219>,
              get_trigger_characters = <function 220>,
              is_available = <function 221>,
              new = <function 222>,
              resolve = <function 223>
            }
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      }, {
        cache = {
          entries = {},
          <metatable> = {
            __index = <table 1>
          }
        },
        complete_dedup = <function 224>,
        context = {
          aborted = false,
          bufnr = -1,
          cache = {
            entries = {},
            <metatable> = {
              __index = <table 1>
            }
          },
          cursor = {
            col = -1,
            row = -1
          },
          cursor_after_line = '")))',
          cursor_before_line = 'lua vim.print(vim.inspect(require("cmp',
          cursor_line = 'lua vim.print(vim.inspect(require("cmp")))',
          filetype = "lua",
          id = 5780,
          input = "",
          option = {},
          prev_context = {},
          time = 126199957,
          <metatable> = {
            __index = <table 3>
          }
        },
        entries = {},
        id = 13,
        incomplete = false,
        is_triggered_by_symbol = false,
        name = "nvim_lsp",
        offset = -1,
        request_offset = -1,
        revision = 8,
        source = {
          client = {
            _exec_cmd = <function 225>,
            _on_attach = <function 226>,
            attached_buffers = {
              [6] = true,
              [9] = true,
              [15] = true,
              [190] = true
            },
            cancel_request = <function 227>,
            commands = {},
            config = {
              capabilities = {
                general = {
                  positionEncodings = { "utf-16" }
                },
                textDocument = {
                  callHierarchy = {
                    dynamicRegistration = false
                  },
                  codeAction = {
                    codeActionLiteralSupport = {
                      codeActionKind = {
                        valueSet = { "", "quickfix", "refactor", "refactor.extract", "refactor.inline", "refactor.rewrite", "source", "source.organizeImports" }
                      }
                    },
                    dataSupport = true,
                    dynamicRegistration = true,
                    isPreferredSupport = true,
                    resolveSupport = {
                      properties = { "edit" }
                    }
                  },
                  completion = {
                    completionItem = {
                      commitCharactersSupport = false,
                      deprecatedSupport = false,
                      documentationFormat = { "markdown", "plaintext" },
                      preselectSupport = false,
                      snippetSupport = false
                    },
                    completionItemKind = {
                      valueSet = {}
                    },
                    contextSupport = false,
                    dynamicRegistration = false
                  },
                  declaration = {
                    linkSupport = true
                  },
                  definition = {
                    dynamicRegistration = true,
                    linkSupport = true
                  },
                  diagnostic = {
                    dynamicRegistration = false
                  },
                  documentHighlight = {
                    dynamicRegistration = false
                  },
                  documentSymbol = {
                    dynamicRegistration = false,
                    hierarchicalDocumentSymbolSupport = true,
                    symbolKind = {
                      valueSet = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26 }
                    }
                  },
                  formatting = {
                    dynamicRegistration = true
                  },
                  hover = {
                    contentFormat = { "markdown", "plaintext" },
                    dynamicRegistration = true
                  },
                  implementation = {
                    linkSupport = true
                  },
                  inlayHint = {
                    dynamicRegistration = true,
                    resolveSupport = {
                      properties = { "textEdits", "tooltip", "location", "command" }
                    }
                  },
                  publishDiagnostics = {
                    dataSupport = true,
                    relatedInformation = true,
                    tagSupport = {
                      valueSet = { 1, 2 }
                    }
                  },
                  rangeFormatting = {
                    dynamicRegistration = true
                  },
                  references = {
                    dynamicRegistration = false
                  },
                  rename = {
                    dynamicRegistration = true,
                    prepareSupport = true
                  },
                  semanticTokens = {
                    augmentsSyntaxTokens = true,
                    dynamicRegistration = false,
                    formats = { "relative" },
                    multilineTokenSupport = false,
                    overlappingTokenSupport = true,
                    requests = {
                      full = {
                        delta = true
                      },
                      range = false
                    },
                    serverCancelSupport = false,
                    tokenModifiers = { "declaration", "definition", "readonly", "static", "deprecated", "abstract", "async", "modification", "documentation", "defaultLibrary" },
                    tokenTypes = { "namespace", "type", "class", "enum", "interface", "struct", "typeParameter", "parameter", "variable", "property", "enumMember", "event", "function", "method", "macro", "keyword", "modifier", "comment", "string", "number", "regexp", "operator", "decorator" }
                  },
                  signatureHelp = {
                    dynamicRegistration = false,
                    signatureInformation = {
                      activeParameterSupport = true,
                      documentationFormat = { "markdown", "plaintext" },
                      parameterInformation = {
                        labelOffsetSupport = true
                      }
                    }
                  },
                  synchronization = {
                    didSave = true,
                    dynamicRegistration = false,
                    willSave = true,
                    willSaveWaitUntil = true
                  },
                  typeDefinition = {
                    linkSupport = true
                  }
                },
                window = {
                  showDocument = {
                    support = true
                  },
                  showMessage = {
                    messageActionItem = {
                      additionalPropertiesSupport = false
                    }
                  },
                  workDoneProgress = true
                },
                workspace = {
                  applyEdit = true,
                  configuration = true,
                  didChangeConfiguration = {
                    dynamicRegistration = false
                  },
                  didChangeWatchedFiles = {
                    dynamicRegistration = true,
                    relativePatternSupport = true
                  },
                  inlayHint = {
                    refreshSupport = true
                  },
                  semanticTokens = {
                    refreshSupport = true
                  },
                  symbol = {
                    dynamicRegistration = false,
                    symbolKind = {
                      valueSet = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26 }
                    }
                  },
                  workspaceEdit = {
                    resourceOperations = { "rename", "create", "delete" }
                  },
                  workspaceFolders = true
                }
              },
              cmd = <function 228>,
              filetypes = { "markdown", "graphql", "handlebars", "scss", "markdown.mdx", "typescript", "css", "json", "jsonc", "html", "javascriptreact", "vue", "javascript", "less", "typescriptreact", "yaml", "go", "sh", "lua", "org", "just", "yml", "vim", "dockerfile", "tex", "terraform", "taskedit", "python", "gitrebase", "text", "dosbatch", "ps1", "rst", "java", "ruby", "terraform-vars", "tf", "gitcommit", "toml", "templ" },
              flags = {
                debounce_text_changes = 250
              },
              get_language_id = <function 229>,
              name = "null-ls",
              on_attach = <function 230>,
              on_exit = <function 231>,
              on_init = <function 232>,
              root_dir = "/Users/chazleong/my/codeium.nvim",
              settings = {}
            },
            dynamic_capabilities = {
              capabilities = {},
              client_id = 3,
              <metatable> = {
                __index = <table 16>
              }
            },
            handlers = {},
            id = 3,
            initialized = true,
            is_stopped = <function 233>,
            messages = {
              messages = {},
              name = "null-ls",
              progress = {},
              status = {}
            },
            name = "null-ls",
            notify = <function 234>,
            offset_encoding = "utf-16",
            progress = {
              _idx_read = 31,
              _idx_write = 30,
              _items = { {
                  token = 154,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 154,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 155,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 155,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 155,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 156,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 156,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 156,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 157,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 157,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 157,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 158,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 158,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 158,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 159,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 159,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 159,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 160,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 160,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 160,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 161,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 161,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 161,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 162,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 162,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 162,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 163,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 163,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 163,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 147,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 147,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 147,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 148,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 148,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 148,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 149,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 149,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 149,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 150,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 150,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 150,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 151,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 151,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 151,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 152,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 152,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 152,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                }, {
                  token = 153,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 153,
                  value = {
                    kind = "report",
                    message = "trail-space",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }, {
                  token = 153,
                  value = {
                    kind = "end",
                    percentage = 100,
                    title = "diagnostics"
                  }
                },
                [0] = {
                  token = 154,
                  value = {
                    kind = "begin",
                    percentage = 0,
                    title = "diagnostics"
                  }
                }
              },
              _size = 51,
              pending = {},
              <metatable> = {
                __call = <function 235>,
                __index = <table 17>
              }
            },
            request = <function 236>,
            request_sync = <function 237>,
            requests = {},
            rpc = {
              is_closing = <function 238>,
              notify = <function 239>,
              request = <function 240>,
              terminate = <function 241>
            },
            server_capabilities = {
              codeActionProvider = {
                resolveProvider = false
              },
              completionProvider = {
                allCommitCharacters = {},
                completionItem = {
                  labelDetailsSupport = true
                },
                resolveProvider = false,
                triggerCharacters = { ".", ":", "-" }
              },
              documentFormattingProvider = true,
              documentRangeFormattingProvider = true,
              executeCommandProvider = {
                commands = { "NULL_LS_CODE_ACTION" }
              },
              hoverProvider = true,
              textDocumentSync = {
                change = 1,
                openClose = true,
                save = {
                  includeText = true
                }
              }
            },
            stop = <function 242>,
            supports_method = <function 243>,
            workspace_folders = { {
                name = "/Users/chazleong/my/codeium.nvim",
                uri = "file:///Users/chazleong/my/codeium.nvim"
              } }
          },
          request_ids = {},
          <metatable> = {
            __index = <table 18>
          }
        },
        status = 1,
        <metatable> = {
          __index = <table 6>
        }
      } },
    suspending = false,
    view = {
      custom_entries_view = {
        active = false,
        bottom_up = false,
        column_width = {
          abbr = 71,
          kind = 12,
          menu = 5
        },
        entries = {},
        entries_win = {
          buffer_opt = {
            buftype = "nofile",
            filetype = "cmp_menu",
            tabstop = 1
          },
          name = 1,
          opt = {
            concealcursor = "n",
            conceallevel = 2,
            cursorline = false,
            cursorlineopt = "line",
            foldenable = false,
            scrolloff = 999,
            winblend = 20,
            winhighlight = "Normal:Pmenu,FloatBorder:Pmenu,CursorLine:PmenuSel,Search:None",
            wrap = false
          },
          style = {
            border = { "╭", "─", "╮", "│", "╯", "─", "╰", "│" },
            col = 96,
            height = 20,
            relative = "editor",
            row = 46,
            style = "minimal",
            width = 92,
            zindex = 1001
          },
          <metatable> = {
            __index = <19>{
              buffer_option = <function 244>,
              close = <function 245>,
              get_border_info = <function 246>,
              get_buffer = <function 247>,
              get_content_height = <function 248>,
              info = <function 249>,
              new = <function 250>,
              open = <function 251>,
              option = <function 252>,
              set_style = <function 253>,
              update = <function 254>,
              visible = <function 255>
            }
          }
        },
        event = {
          events = {
            change = { <function 256> }
          },
          <metatable> = {
            __index = <table 5>
          }
        },
        offset = -1,
        <metatable> = {
          __index = {
            _insert = {
              pending = false,
              <metatable> = {
                __call = <function 257>
              }
            },
            _select = <function 258>,
            abort = <function 259>,
            close = <function 260>,
            draw = <function 261>,
            get_active_entry = <function 262>,
            get_entries = <function 263>,
            get_first_entry = <function 264>,
            get_offset = <function 265>,
            get_selected_entry = <function 266>,
            info = <function 267>,
            is_direction_top_down = <function 268>,
            new = <function 269>,
            ns = 6,
            on_change = <function 270>,
            open = <function 271>,
            ready = <function 272>,
            select_next_item = <function 273>,
            select_prev_item = <function 274>,
            visible = <function 275>
          }
        }
      },
      docs_view = {
        window = {
          buffer_opt = {
            buftype = "nofile",
            filetype = "cmp_docs"
          },
          name = 3,
          opt = {
            concealcursor = "n",
            conceallevel = 2,
            foldenable = false,
            linebreak = true,
            scrolloff = 0,
            showbreak = "NONE",
            winblend = 20,
            winhighlight = "FloatBorder:NormalFloat",
            wrap = true
          },
          style = {
            border = { "╭", "─", "╮", "│", "╯", "─", "╰", "│" },
            col = 99,
            height = 2,
            relative = "editor",
            row = 46,
            style = "minimal",
            width = 27,
            zindex = 50
          },
          <metatable> = {
            __index = <table 19>
          }
        },
        <metatable> = {
          __index = {
            close = <function 276>,
            new = <function 277>,
            open = <function 278>,
            scroll = <function 279>,
            visible = <function 280>
          }
        }
      },
      event = {
        events = {
          complete_done = { <function 281> },
          keymap = { <function 282> },
          menu_closed = { <function 283> },
          menu_opened = { <function 284> }
        },
        <metatable> = {
          __index = <table 5>
        }
      },
      ghost_text_view = {
        <metatable> = {
          __index = {
            hide = <function 285>,
            new = <function 286>,
            ns = 8,
            show = <function 287>,
            text_gen = <function 288>
          }
        }
      },
      is_docs_view_pinned = false,
      native_entries_view = {
        entries = {},
        event = {
          events = {},
          <metatable> = {
            __index = <table 5>
          }
        },
        items = {},
        offset = -1,
        preselect_index = 0,
        <metatable> = {
          __index = {
            abort = <function 289>,
            close = <function 290>,
            get_active_entry = <function 291>,
            get_entries = <function 292>,
            get_first_entry = <function 293>,
            get_offset = <function 294>,
            get_selected_entry = <function 295>,
            info = <function 296>,
            new = <function 297>,
            on_change = <function 298>,
            open = <function 299>,
            preselect = <function 300>,
            ready = <function 301>,
            select_next_item = <function 302>,
            select_prev_item = <function 303>,
            visible = <function 304>
          }
        }
      },
      resolve_dedup = <function 305>,
      wildmenu_entries_view = {
        active = false,
        entries = {},
        entries_win = {
          buffer_opt = {
            tabstop = 1
          },
          name = 2,
          opt = {
            concealcursor = "n",
            conceallevel = 2,
            cursorlineopt = "line",
            foldenable = false,
            scrolloff = 0,
            sidescrolloff = 0,
            winhighlight = "Normal:Pmenu,FloatBorder:Pmenu,CursorLine:PmenuSel,Search:None",
            wrap = false
          },
          style = {},
          <metatable> = {
            __index = <table 19>
          }
        },
        event = {
          events = {},
          <metatable> = {
            __index = <table 5>
          }
        },
        offset = -1,
        offsets = {},
        selected_index = 0,
        <metatable> = {
          __index = {
            _get_separator = <function 306>,
            _select = <function 307>,
            abort = <function 308>,
            close = <function 309>,
            draw = <function 310>,
            get_active_entry = <function 311>,
            get_entries = <function 312>,
            get_first_entry = <function 313>,
            get_offset = <function 314>,
            get_selected_entry = <function 315>,
            info = <function 316>,
            new = <function 317>,
            ns = 7,
            on_change = <function 318>,
            open = <function 319>,
            ready = <function 320>,
            select_next_item = <function 321>,
            select_prev_item = <function 322>,
            visible = <function 323>
          }
        }
      },
      <metatable> = {
        __index = {
          _get_entries_view = <function 324>,
          abort = <function 325>,
          close = <function 326>,
          close_docs = <function 327>,
          get_active_entry = <function 328>,
          get_entries = <function 329>,
          get_first_entry = <function 330>,
          get_offset = <function 331>,
          get_selected_entry = <function 332>,
          new = <function 333>,
          on_change = <function 334>,
          on_entry_change = {
            running = false,
            stop = <function 335>,
            sync = <function 336>,
            timeout = 20,
            <metatable> = {
              __call = <function 337>
            }
          },
          open = <function 338>,
          open_docs = <function 339>,
          ready = <function 340>,
          scroll_docs = <function 341>,
          select_next_item = <function 342>,
          select_prev_item = <function 343>,
          visible = <function 344>
        }
      }
    },
    <metatable> = {
      __index = {
        autoindent = <function 345>,
        complete = <function 346>,
        complete_common_string = <function 347>,
        confirm = <function 348>,
        filter = {
          running = false,
          stop = <function 349>,
          sync = <function 350>,
          timeout = 30,
          <metatable> = {
            __call = <function 351>
          }
        },
        get_context = <function 352>,
        get_sources = <function 353>,
        new = <function 354>,
        on_change = <function 355>,
        on_keymap = <function 356>,
        on_moved = <function 357>,
        prepare = <function 358>,
        register_source = <function 359>,
        reset = <function 360>,
        set_context = <function 361>,
        suspend = <function 362>,
        unregister_source = <function 363>
      }
    }
  },
  event = <table 4>,
  get_active_entry = <function 364>,
  get_config = <function 365>,
  get_entries = <function 366>,
  get_selected_entry = <function 367>,
  lsp = {
    CompletionItemKind = { "Text", "Method", "Function", "Constructor", "Field", "Variable", "Class", "Interface", "Module", "Property", "Unit", "Value", "Enum", "Keyword", "Snippet", "Color", "File", "Reference", "Folder", "EnumMember", "Constant", "Struct", "Event", "Operator", "TypeParameter",
      Class = 7,
      Color = 16,
      Constant = 21,
      Constructor = 4,
      Enum = 13,
      EnumMember = 20,
      Event = 23,
      Field = 5,
      File = 17,
      Folder = 19,
      Function = 3,
      Interface = 8,
      Keyword = 14,
      Method = 2,
      Module = 9,
      Operator = 24,
      Property = 10,
      Reference = 18,
      Snippet = 15,
      Struct = 22,
      Text = 1,
      TypeParameter = 25,
      Unit = 11,
      Value = 12,
      Variable = 6
    },
    CompletionItemTag = {
      Deprecated = 1
    },
    CompletionTriggerKind = {
      Invoked = 1,
      TriggerCharacter = 2,
      TriggerForIncompleteCompletions = 3
    },
    InsertTextFormat = {
      PlainText = 1,
      Snippet = 2
    },
    InsertTextMode = {
      AdjustIndentation = 2,
      AsIs = 1
    },
    MarkupKind = {
      Markdown = "markdown",
      PlainText = "plaintext"
    },
    Position = {
      to_lsp = <function 368>,
      to_utf16 = <function 369>,
      to_utf32 = <function 370>,
      to_utf8 = <function 371>,
      to_vim = <function 372>
    },
    PositionEncodingKind = {
      UTF16 = "utf-16",
      UTF32 = "utf-32",
      UTF8 = "utf-8"
    },
    Range = {
      to_lsp = <function 373>,
      to_vim = <function 374>
    }
  },
  mapping = <table 2>,
  open_docs = <function 375>,
  register_source = <function 376>,
  scroll_docs = <function 377>,
  select_next_item = <function 378>,
  select_prev_item = <function 379>,
  setup = {
    buffer = <function 380>,
    cmdline = <function 381>,
    filetype = <function 382>,
    global = <function 383>,
    <metatable> = {
      __call = <function 384>
    }
  },
  status = <function 385>,
  suspend = <function 386>,
  sync = <function 387>,
  unregister_source = <function 388>,
  vim = true,
  visible = <function 389>,
  visible_docs = <function 390>
}
```
