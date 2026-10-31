# Janish's VideoExpress Couple Comedy Agent

Editable browser-agent instructions for producing funny husband-and-wife stickman Shorts in VideoExpress AI. Forked from [ai-playbooks/videoexpress-stickman-story-agent](https://github.com/ai-playbooks/videoexpress-stickman-story-agent); see [UPSTREAM.md](UPSTREAM.md).

This repository stores instructions, examples and checks. It does not contain a running service, API integration or GitHub Actions video generator. GitHub does not render or schedule videos by itself. A browser-capable agent must execute the instructions in a signed-in VideoExpress session, and login/product limits may require intervention.

## Start a video
1. Start a chat with browser control and GitHub access.
2. Tell the agent to read and follow this repository's [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md), [couple reference rules](characters/permanent-couple.md), [production workflow](workflows/couple-comedy.md) and [checklist](evals/acceptance-checklist.md). A bare link is not an instruction to execute.
3. Give a story idea and attach the approved couple image, or identify its exact saved asset in VideoExpress My AI Images. The permanent reference is not bundled in this public repository; the agent must inspect the actual image.
4. Ask it to open https://app.videoexpress.ai/ and finish any required sign-in through supported authentication controls.
5. Let it generate, assemble, subtitle, add available included music, save and export. Intervene only for required user actions or concrete blockers.
6. Review the delivered MP4 and the report of any unavailable checks.

Copy the [example request](examples/example-request.md). If GitHub cannot be read, copy the raw SYSTEM_PROMPT.md contents into the chat and supply the companion reference/workflow/checklist files. Pasted instructions apply to that chat; they do not install a permanent system prompt.

## Defaults
| Setting | Default |
| --- | --- |
| Story | Affectionate husband-and-wife comedy |
| Composition | Vertical 9:16, consistent 2D stickman style |
| Timing | Approximately 30 seconds, five roughly six-second clips |
| Characters | Reuse the approved permanent couple across stories |
| Queue | At most five concurrent video jobs, fewer if the visible limit is lower |
| Voice | Available VideoExpress system voice; Beau Whitaker if available |
| Text/music | Correctly spelled subtitles and suitable included background music when supported |
| Completion | Saved project plus exported MP4, with final playback checks |

Explicit requests override defaults. Runtime is measured, not guaranteed from narration length. Food/props appear only at their intended story event. Preserve glasses, faces, clothing and complete stick limbs. Every clip, including the last, must reach the timeline exactly once. Blank/dark exported sections require investigation.

## Edit your workflow
Change SYSTEM_PROMPT.md for production behavior, characters/permanent-couple.md for confirmed character rules, workflows/couple-comedy.md for pacing, and evals/acceptance-checklist.md for acceptance criteria. Keep them consistent in the same pull request. Use templates/scene-ledger.md privately for run state; never commit credentials, private asset IDs or session data.

The files under workflows/ are human-readable procedures, not GitHub Actions YAML. The agent should not modify GitHub during ordinary video creation. Review upstream changes manually before integrating them; do not overwrite personal defaults.

## Examples
- [Massage Swap](examples/massage-swap.md): current five-scene couple comedy.
- [Continuous cat story](examples/continuous-cat-story.md): optional action-continuity illustration.
- Beach, heist and zoo files retain historical story material. They are not authoritative settings or completion instructions.

## Validation and limits
Use the acceptance checklist on an actual production run. Repository consistency checks cannot prove VideoExpress UI availability, reference fidelity, speech quality or MP4 quality. This customization has not itself rendered a test video. Follow visible product controls and report unsupported features honestly.
