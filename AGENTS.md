# Agent Instructions

## Git Workflow

- After making any code changes, create a git commit for those changes before finishing the task.
- Keep each commit focused on the work completed in that turn.
- Run the relevant validation checks before committing when practical.
- If validation cannot be run, mention that in the final response and still commit the completed code changes unless the user asks otherwise.
- Do not include unrelated user changes in the commit.
- Use a concise commit message that describes the change.

## Project Notes

- The current shipped app is Electron, but the native migration target is `native/`, built with C#/.NET and Avalonia UI.
- Prefer existing project patterns over introducing new frameworks or large abstractions.
- Rebuild the portable app with `pnpm run dist:portable` when source changes need to be reflected in `dist-portable/EVE-Portable.exe`.
- For native changes, run `dotnet build native\EVE.Native.sln` only. Do not run tests by default; if the build fails, focus on the reported build errors first.
