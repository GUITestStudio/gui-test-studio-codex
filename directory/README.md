<p align="center"><img src="assets/icon.png" alt="GUI Test Studio" width="128" height="128"></p>

# GUI Test Studio for ChatGPT and Codex

Create, change and run **automated end-to-end tests** of Windows apps and web pages by asking Codex. Describe the
test in a prompt ("open the calculator, compute 12 × 7 and check that it shows 84") and Codex performs the steps on
your real screen with GUI Test Studio's tools, checks every result as it goes, and saves a test you can run again,
from a terminal or a CI/CD pipeline, and open in GUI Test Studio to edit it visually.

- **Create a test from a prompt**: Codex clicks, types, scrolls and drags, then checks texts, values, pictures,
  counts and layouts. A check that could not pass on the screen right now is refused with the reason.
- **Run it** and get a verdict, or open it in GUI Test Runner-Recorder for the full Confidence Report.
- **See why a run failed**: what each check expected and what the run found, with the pictures, what the AI said, and
  since when the test fails.
- **Change it in place** ("raise the wait to 5 seconds", "also check the total after step 5", "accept the new button"):
  Codex lists the changes and asks before anything is written.
- **Report and ship it**: a bug report as a PDF, a workbook or a Jira issue (only once you agree), a runner test for a CI
  machine, and the command and pipeline piece for GitLab, Azure DevOps, Jenkins, TeamCity or GitHub Actions.
- **Web apps on every browser and device**: Chrome, Edge and Firefox, phones, tablets and desktop sizes.
- **From a Figma design**: a test made from a design exported with GUI Test Studio's Figma plugin.

## Requirements

- **Windows 10 or 11.**
- **GUI Test Studio installed**, from [guiteststudio.com/download](https://www.guiteststudio.com/download), and
  connected to Codex (below).
- **A GUI Test Studio account**, signed in on this computer. Without one, every tool answers with how to sign in, and
  nothing else runs.

Works in the **ChatGPT desktop app** (Codex), the **Codex command line** and **Codex's VS Code extension**: the three
read one setting. A local tool like this one does not run in ChatGPT on the web or on a phone.

## Get started

1. Install GUI Test Studio and sign in (the app asks at its first start).
2. Connect it to Codex: in GUI Test Runner-Recorder, click **Create Test From Prompt**, then **Connect** on the
   **ChatGPT & Codex** card. Or, in a terminal:

   ```
   codex mcp add gui-test-studio -- "C:\Program Files\GUI Test Studio\Runner\gts-mcp.exe"
   ```

3. Restart Codex and ask: "With GUI Test Studio, open the calculator, compute 5 + 5 and verify the result shows 10."

## What this plugin holds, and what is sent

This plugin is a skill: it tells Codex when and how to use GUI Test Studio's tools. It runs nothing itself. The tools
are GUI Test Studio's own program on your computer, which you connect in step 2. Everything they do happens there:

- **On your computer**: it moves the mouse, types and reads your screen (the windows' accessibility information, the
  page of a browser it opened, the screen's picture) to perform and check the test's steps, and writes the test files
  where you choose.
- **guiteststudio.com**: it checks that you are signed in, whether a newer version of GUI Test Studio is published,
  and, unless you turn them off, sends anonymous usage statistics (for example that a test was created from a prompt
  and through which kind of AI assistant app). Never a test, a screenshot, a prompt or anything you type. See the
  [privacy policy](https://www.guiteststudio.com/privacy); the switch is under Preferences, General, Privacy in either
  application.
- **An AI provider**, only when you turn AI Smart Verification on in GUI Test Studio and choose OpenAI or Anthropic
  with your own key: the two pictures of a visual check that failed, to explain the difference.

Nothing is sent anywhere else.

## Documentation and support

- [Create a test from a prompt](https://www.guiteststudio.com/docs/claude), the guide (it says Claude; ChatGPT does the same)
- [support@guiteststudio.com](mailto:support@guiteststudio.com)

## Licence

Proprietary. Copyright (c) 2026 GUI Test Studio SARL. All rights reserved. See [LICENSE](LICENSE).
