# Tool Builder: when chat is not enough

## Purpose
Build a local, single-file HTML tool page Alex opens in a browser to work
with data hands-on: drag, stretch, reorder, mark up. Example here: a table
of FAQ entries with pass/fail status Alex can filter and mark up directly.

## When to use
Alex needs to SEE and MOVE the data, not read about it. Or Alex says "build
me a tool for this." Propose it, do not wait to be asked twice.

## Requirements, every tool page
1. One self-contained .html file saved in deliverables/tools/. No internet,
   no accounts, no outside calls. It works offline in a normal browser by
   double-clicking it.
2. All the data lives in one JSON object near the top of the page's script,
   so state is easy to find, update, and regenerate.
3. Two buttons on every tool page, always:
   - "Copy prompt for my agent." Copies a ready-to-paste prompt to the
     clipboard: the tool's name and file path (deliverables/tools/[name].html),
     the date, the full current state as JSON, and one closing line: "Update
     your saved copy of this tool to match this state, then tell me what
     changed and what you recommend next." The button shows visible
     confirmation (the label flips to "Copied"), and if the clipboard write
     fails it displays the full prompt in a selectable text box to copy by
     hand.
   - "Export." Downloads the data as CSV or JSON for use outside the agent.
4. Round-trip rule: when Alex pastes a copy-prompt back, the pasted path
   tells you which file to update. Update that file starting from the
   pasted state. Never rebuild from scratch and never overwrite edits with
   an older version.
5. Large data: past roughly 100 rows, skip the copy-prompt. Export as JSON
   instead, then read the file from the project folder.
6. Unsaved-work guard: a permanent one-line notice next to the buttons
   ("Edits live only in this tab. Copy prompt or Export before closing")
   plus a browser close warning whenever state differs from the loaded state.

## Rules
- When delivering a tool page, teach the save loop first, in two sentences.
- A tool page displays and edits. It never sends anything anywhere.
- No secrets and no restricted data in any tool page, ever.
