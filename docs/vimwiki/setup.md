# Setup

## Directory Structure

```
~/vimwiki/
├── index.md                    # Main dashboard
├── inbox.md                    # Quick capture (process daily)
├── todo.md                     # Active tasks (GTD next actions)
├── someday.md                  # GTD someday/maybe list
│
├── diary/                      # Daily entries
│   ├── diary.md                # Diary index
│   └── 2026-02-25.md
│
├── school/                     # Coursework
│   ├── index.md
│   ├── schedule.md
│   ├── physics-510/
│   │   ├── index.md
│   │   ├── lecture-notes.md
│   │   ├── problem-sets.md
│   │   └── exam-prep.md
│   ├── physics-522/
│   │   └── ...
│   └── thesis/
│       ├── ideas.md
│       ├── literature.md
│       └── progress.md
│
├── research/                   # Research Zettelkasten
│   ├── index.md
│   ├── inbox.md                # Research ideas to process
│   ├── concepts/               # Atomic concept notes
│   ├── methods/                # Computational techniques
│   ├── literature/             # Paper notes
│   └── projects/               # Active research projects
│
├── code/                       # Developer notes
│   ├── index.md
│   ├── snippets/
│   ├── tools/
│   └── projects/
│
├── reading/                    # Books & articles
│   ├── index.md
│   ├── to-read.md
│   ├── currently-reading.md
│   ├── completed.md
│   └── notes/
│
├── reference/                  # Permanent reference material
│   ├── contacts.md
│   └── cheatsheets/
│
├── templates/                  # Note templates
│   ├── diary.md
│   ├── lecture.md
│   ├── paper-review.md
│   ├── concept.md
│   ├── project.md
│   ├── meeting.md
│   └── problem-set.md
│
└── archive/                    # Completed/old material
    └── ...
```

---

## Vim Configuration

Add to your `~/.vimrc` or `~/.config/nvim/init.vim`:

```vim
" ============================================
" VIMWIKI CONFIGURATION
" ============================================

" Main wiki configuration
let g:vimwiki_list = [{
  \ 'path': '~/vimwiki/',
  \ 'syntax': 'markdown',
  \ 'ext': '.md',
  \ 'auto_diary_index': 1,
  \ 'auto_generate_links': 1,
  \ 'auto_tags': 1,
  \ }]

" Use markdown syntax everywhere
let g:vimwiki_global_ext = 0
let g:vimwiki_markdown_link_ext = 1

" Auto-generate header based on filename
let g:vimwiki_auto_header = 1

" Folding
let g:vimwiki_folding = 'expr'

" Tags
let g:vimwiki_tag_format = {'pre': ':', 'pre_mark': '', 'post_mark': '', 'post': ':'}

" ============================================
" TEMPLATE AUTO-INSERTION
" ============================================

" Diary template
autocmd BufNewFile ~/vimwiki/diary/[0-9]*.md :silent 0r ~/vimwiki/templates/diary.md
autocmd BufNewFile ~/vimwiki/diary/[0-9]*.md :silent %s/{{DATE}}/\=strftime('%Y-%m-%d')/g

" Lecture template
autocmd BufNewFile ~/vimwiki/school/*/lecture-*.md :silent 0r ~/vimwiki/templates/lecture.md

" Research concept template
autocmd BufNewFile ~/vimwiki/research/concepts/*.md :silent 0r ~/vimwiki/templates/concept.md

" Paper review template
autocmd BufNewFile ~/vimwiki/research/literature/*.md :silent 0r ~/vimwiki/templates/paper-review.md

" ============================================
" CUSTOM KEYBINDINGS
" ============================================

" Quick access to common pages
nnoremap <Leader>wi :e ~/vimwiki/inbox.md<CR>
nnoremap <Leader>wt :e ~/vimwiki/todo.md<CR>
nnoremap <Leader>wc :e ~/vimwiki/school/index.md<CR>
nnoremap <Leader>wr :e ~/vimwiki/research/index.md<CR>
nnoremap <Leader>wb :e ~/vimwiki/reading/index.md<CR>

" Search all wiki files
nnoremap <Leader>wf :vimgrep //g ~/vimwiki/**/*.md<Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left><Left>

" Search by tag
nnoremap <Leader>wT :VimwikiSearchTags<Space>

" Generate diary index
nnoremap <Leader>wI :VimwikiDiaryGenerateLinks<CR>

" Quick timestamp insert
nnoremap <Leader>ts :r! date "+\%H:\%M"<CR>kJ

" ============================================
" ZETTELKASTEN SUPPORT (Optional: vim-zettel)
" ============================================
" Uncomment if you install vim-zettel plugin

" let g:zettel_format = "%Y%m%d%H%M"
" let g:zettel_default_mappings = 0
" let g:zettel_fzf_command = "rg --column --line-number --ignore-case --no-heading --color=always"

" ============================================
" QUALITY OF LIFE
" ============================================

" Spell check in wiki files
autocmd FileType vimwiki setlocal spell spelllang=en_us

" Soft wrap for readability
autocmd FileType vimwiki setlocal wrap linebreak

" Conceal links for cleaner reading
set conceallevel=2
```
