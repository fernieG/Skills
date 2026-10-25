# Skills

Two simple Claude skills that take a business idea to a working app, with you deciding at every step.

| Skill | What it does | You get |
|-------|--------------|---------|
| [`challenge-my-idea`](challenge-my-idea/SKILL.md) | Interviews you about your idea, one question at a time, each with a suggested answer | A requirements brief a project manager can start from |
| [`deliver-my-idea`](deliver-my-idea/SKILL.md) | Builds a prototype from the brief and takes it to production through your checkpoints | A validated app, test results and a go/no-go record |

## How it works

1. **Challenge the idea.** About 12 to 15 short questions: problem, goal, what already exists, scope, users, processes, connected applications, rules and calculations, data, constraints, acceptance criteria, risks. "I don't know, ask the application owner" is a fine answer. Facts that can't be checked against an official source are marked "to verify".
2. **Get the brief.** One to three pages, with requirements marked *now* or *later*, and the open points listed with who to ask.
3. **See a prototype.** Built from the *now* items, to open on your own phone or computer. It comes with real data only if it is public; otherwise realistic synthetic data, labelled on screen. You can also load your own data into it on your device: it is read there, never sent anywhere or saved. These skills don't store any data.
4. **Validate the screens.** Changes until you say they are right.
5. **Validate the test cases.** Built from the brief's acceptance criteria, rules and calculations, including what must never happen.
6. **Go or no-go.** The tests are run and reported as passed, failed or not run. You decide whether it goes to production.

Nothing moves to the next step without your explicit approval.

## Add the skills to Claude

1. Download this repository as a ZIP, then make one ZIP per skill folder (`challenge-my-idea`, `deliver-my-idea`). Keep the folder names as they are: they must match the skill names.
2. In Claude, open **Customize > Skills**, click **+**, then **+ Create skill**, then **Upload a skill**, and choose the ZIP.
3. Turn the skill on in your skills list.

Skills need code execution to be enabled. On Free, Pro and Max plans, turn on "Code execution and file creation" in Settings > Capabilities. On Team and Enterprise plans, your organization's owner controls this. Full instructions: [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

Then just write: *"Challenge my idea: …"*

## Please don't share confidential information in the chat

No client names, personal data, passwords or internal figures in your messages to Claude. Placeholders like "Client A" or "App X" are fine. To try the prototype on your own data, load it into the prototype on your device instead.

## Credits

The one-question-at-a-time interview approach is inspired by the "grill me" skill in [mattpocock/skills](https://github.com/mattpocock/skills) (MIT). The wording of these skills is original.
