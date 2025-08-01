# VS Code Debug Configuration for BaileysCSharp

This folder contains the necessary configuration files to debug the BaileysCSharp project in Visual Studio Code.

## Files Created

### 1. `launch.json`
Contains debug configurations:
- **Launch WhatsSocketConsole**: Debug the console application in integrated terminal
- **Launch WhatsSocketConsole (External Terminal)**: Debug in external terminal
- **Attach to Process**: Attach debugger to running process

### 2. `tasks.json`
Contains build and utility tasks:
- **build**: Build the entire solution (default build task)
- **build-console**: Build only the console project
- **publish**: Publish the solution in Release mode
- **watch**: Watch and auto-rebuild the console project
- **clean**: Clean the solution
- **restore**: Restore NuGet packages
- **run-tests**: Run unit tests

### 3. `settings.json`
Workspace-specific settings for optimal C# development experience.

### 4. `extensions.json`
Recommended extensions for the best development experience.

## How to Debug

### Method 1: Using F5 (Recommended)
1. Open VS Code in the project root folder
2. Open any C# file (e.g., `WhatsSocketConsole/Program.cs`)
3. Set breakpoints by clicking on the line numbers
4. Press `F5` or go to Run → Start Debugging
5. Select "Launch WhatsSocketConsole" configuration

### Method 2: Using Debug Panel
1. Open the Debug panel (Ctrl+Shift+D / Cmd+Shift+D)
2. Select "Launch WhatsSocketConsole" from the dropdown
3. Click the green play button

### Method 3: Using Command Palette
1. Press Ctrl+Shift+P / Cmd+Shift+P
2. Type "Debug: Start Debugging"
3. Select the launch configuration

## Build Tasks

You can run tasks using:
- `Ctrl+Shift+P` → "Tasks: Run Task" → Select task
- Or use the Terminal menu → Run Task

## Recommended Extensions

The project recommends these extensions (they will be suggested automatically):
- C# Dev Kit
- C# Extension
- .NET Install Tool
- Protocol Buffer support
- Code Spell Checker

## Troubleshooting

### If debugging doesn't work:
1. Make sure all recommended extensions are installed
2. Ensure .NET 9 SDK is installed
3. Run `dotnet build` in terminal to verify project compiles
4. Check that the console project builds successfully

### If protobuf generation fails on ARM64 macOS:
The project is configured to automatically handle this. If you see protobuf errors:
1. Make sure Homebrew protoc is installed: `brew install protobuf`
2. The build will automatically use system protoc on ARM64 macOS

## Project Structure

```
BaileysCSharp/
├── BaileysCSharp/          # Main library project
├── WhatsSocketConsole/     # Console application (debug target)
├── BaileysCSharp.Tests/    # Unit tests
└── .vscode/               # VS Code configuration
```

The console application (`WhatsSocketConsole`) references the main library and serves as the entry point for debugging and testing.