# tryout-remix-material-ui

**A simple demo which renders Markdown using Remix and Material UI (MUI)**

- Version: 0.0.1
- Created: 13th June 2025 by Rich Plastow
- Updated: 13th June 2025 by Rich Plastow
- <https://github.com/richplastow/tryout-remix-material-ui>

---

This is a basic example app which renders Markdown using
[Remix](https://remix.run/docs/en/main) (which is now
[React Router v7](https://reactrouter.com/home)) and
[Material UI.](https://mui.com/material-ui/getting-started/) You can use it as
a starting point for your own projects.

## External resources and documentation

- [Remix Docs](https://remix.run/docs/en/main)
- [React Router](https://reactrouter.com/home)
- [Material UI Overview](https://mui.com/material-ui/getting-started/)
- [Google Material Design M3](https://m3.material.io/)
- [Markdown Getting Started](https://www.markdownguide.org/getting-started/)
- [React Quick Start](https://react.dev/learn)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
- [material-ui-remix-ts](https://github.com/mui/material-ui/tree/master/examples/material-ui-remix-ts)

## From scratch

Here’s a brief step by step guide to creating an app like this from scratch.

### Step 1: Create a new Remix app

Read React Router's
['Decision Advice'](https://reactrouter.com/start/modes#decision-advice) to
decide which of the 3 modes to use. tryout-remix-material-ui uses the
'Framework' mode:  
<https://reactrouter.com/start/framework/installation>

#### Step 1-1: Run the 'default' `npx` installation

There are about a dozen official templates available:  
<https://github.com/remix-run/react-router-templates/tree/main>

```bash
# Install using the default template.
npx create-react-router@latest --template remix-run/react-router-templates/default
# Need to install the following packages:
# create-react-router@7.6.2
# Ok to proceed? (y)
y
# 
# npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory ...
# npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported
# 
#          create-react-router v7.6.2
# 
#    dir   Where should we create your new project?
.
# 
#       ◼  Template: Using remix-run/react-router-templates/default...
#       ✔  Template copied
# 
#  overwrite   Your project directory contains files that will be overwritten by
#              this template (you can force with `--overwrite`)
# 
#              Files that would be overwritten:
#                .gitignore
#                README.md
# 
#              Do you wish to continue?
#              
Yes
#       ◼  Nice! Git has already been initialized
# 
#   deps   Install dependencies with npm?
Yes
# 
#       ✔  Dependencies installed
# 
#   done   That's it!
#          Check out README.md for development and deploy instructions.
# 
#          Join the community at https://rmx.as/discord
```

<!-- node_modules is 119,042,700 bytes (136.8 MB on disk) for 6,735 items -->

Store Remix's default README.md and .gitignore for future reference, and use
a more comprehensive .gitignore instead.

```bash
# Move Remix's default README.md and .gitignore to an appendices folder.
mkdir -p docs/appendices/ && \
mv README.md docs/appendices/01-remix-default-readme.md && \
mv .gitignore docs/appendices/02-remix-default-gitignore.txt
# (no output)

# Use `cat` with `EOF` to create a more comprehensive .gitignore file.
cat > .gitignore <<EOF
# See https://help.github.com/articles/ignoring-files/ for more about ignoring files.

# OS files, security and certificates.
.DS_Store
*.pem

# Dependencies.
/node_modules/
.pnp
.pnp.js

# Test results and coverage.
coverage.json
/coverage/

# React Router (Remix) build artifacts.
/.react-router/
/build/

# Other build artifacts.
dist/

# Debug and error logs.
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Environment variables.
.env.local
.env.development.local
.env.test.local
.env.production.local
EOF
# (no output)
```
