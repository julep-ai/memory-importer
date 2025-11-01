# Neutralino.js Build Skill

You are helping build a Neutralino.js application. Neutralino.js is a lightweight cross-platform desktop application framework that uses JavaScript, HTML, and CSS.

## Available Commands

### neu create
Creates a new Neutralino.js app:
- `neu create <path>` - Create app with default template
- `neu create <path> --template <github-repo>` - Create with custom template

### neu run
Launches the application in development mode:
- `neu run` - Start dev server with auto-reload
- Shows process and extension output streams

### neu build
Generates binaries for distribution:
- `neu build` - Build for all platforms
- `neu build --release` - Create portable ZIP files
- `neu build --embed-resources` - Single-file executables
- `neu build --macos-bundle` - macOS app bundle

### neu update
Updates Neutralino.js binaries and client libraries:
- `neu update` - Update to configured version
- `neu update --latest` - Update to newest version

### neu version
Display version information:
- `neu version` - Show all version info

### neu plugins
Manage CLI extensions:
- `neu plugins --add <plugin>` - Add plugin
- `neu plugins --remove <plugin>` - Remove plugin

## Configuration

Neutralino.js apps are configured via `neutralino.config.json`:
- `cli.distributionPath` - Customize build output directory (default: `dist`)
- `cli.resourcesPath` - Resources location
- Resource modes: `embedded`, `bundle`, or `directory`

## Common Workflows

### Create New App
```bash
neu create myapp
cd myapp
npm install  # Install dependencies
neu run      # Start development
```

### Development
```bash
neu run      # Auto-reload enabled for fast iteration
```

### Build for Production
```bash
neu build --release              # All platforms
neu build --embed-resources      # Single executable
neu build --release --embed-resources  # Portable single files
```

### Update Framework
```bash
neu update --latest
```

## When to Use This Skill

Use this skill when the user asks to:
- Create a new Neutralino.js application
- Build or run a Neutralino.js app
- Update Neutralino.js binaries
- Configure build settings
- Generate platform-specific binaries
- Work with Neutralino.js CLI

## Important Notes

- No compilation required for app development (unlike Electron)
- Hot Module Reloading (HMR) supported with frontend frameworks
- Generates binaries for Linux, macOS, and Windows
- Much smaller bundle sizes compared to Electron
- Uses native OS APIs instead of bundling Chromium
- Install CLI globally: `npm i -g @neutralinojs/neu`

## Task Approach

When helping with Neutralino.js:
1. Check if `@neutralinojs/neu` CLI is installed
2. Verify `neutralino.config.json` exists for existing projects
3. Use appropriate commands based on development phase
4. Consider resource mode for distribution needs
5. Test builds on target platforms when possible
