# jackson_workspace

Jackson's local Claude Code workspace folder. Holds shared defaults plus several independent project repos.

## Contents

- **`CLAUDE.md`** — Claude Code defaults applied to any session started inside this workspace (communication style, behavior rules, project interests).
- **`Google-MCP/`** — Step-by-step guide to setting up the Google Workspace MCP server for Claude Code. Independent repo: [1WERTYU/Google-MCP](https://github.com/1WERTYU/Google-MCP).
- **`hello-world-website/`** — First website project. Independent repo: [1WERTYU/hello-world-website](https://github.com/1WERTYU/hello-world-website).
- **`67willneverdie.com/`** — Personal website. Independent repo: [1WERTYU/67willneverdie.com](https://github.com/1WERTYU/67willneverdie.com).

The three project folders are independent git repos with their own GitHub remotes — they're listed in `.gitignore` here so this workspace repo only tracks shared configuration.

## Moving to a new machine

Claude Code's own config (subagents, skills, settings, memory) lives in
`~/.claude`, which is gitignored here and therefore **not** in this repo. It is
version-controlled separately in [1WERTYU/claude-config](https://github.com/1WERTYU/claude-config) (private):

```bash
git clone https://github.com/1WERTYU/claude-config.git ~/claude-config
~/claude-config/install.sh          # restore agents, skills, settings, memory
~/claude-config/clone-projects.sh   # re-clone this workspace and all nested repos
```

That repo's README also lists the setup steps that can't be version-controlled
(gh auth, nvm/Node, Vercel CLI, Chrome extension, Google connectors).
