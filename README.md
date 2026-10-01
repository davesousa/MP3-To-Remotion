# MP3 to Remotion

Turn an MP3 or other audio recording into a Remotion lyric video or music visualizer with an AI coding agent.

This repository provides a reusable instruction file, not a prebuilt video app. The agent uses the instructions to analyze your track, propose concepts, create the selected video, and export it.

## Getting started

1. Download [mp3_to_remotionvideo.md](mp3_to_remotionvideo.md).
2. Give the file to your AI coding agent, such as Codex, along with your audio recording. Explicitly ask the agent to follow the instructions.
3. Choose a **lyric video** or **visualizer**.
4. Approve one of the three proposed visual concepts.
5. If images are needed, choose automatic generation when the agent has suitable tools, or generate the images yourself using the supplied prompts and provide them to the agent.

Example request:

> Follow the attached mp3_to_remotionvideo.md instructions to create a video from my attached MP3. Ask me for the video type first, then propose three concepts for approval.

You can also install the file as an agent skill if your agent supports Markdown skills. Follow your agent's installation instructions; this repository is not an installable Codex plugin package.

## What the workflow does

- **Video type first:** Asks whether you want a lyric video or a visualizer before pitching concepts.
- **Concept approval:** Offers exactly three distinct concepts tailored to your recording and selected video type, then waits for your choice.
- **Image-tool detection:** Checks the tools actually available in your agent before offering automatic image generation.
- **Automatic images:** Generates and validates required images, then continues through production and export.
- **Manual images:** Provides a separate prompt and constraints for every required image, waits for your files, and checks their suitability before continuing.
- **Production through completion:** Reviews drafts internally, fixes issues, and verifies the final exports. After the image workflow is settled and assets are ready, it avoids optional progress messages until delivery. It may still interrupt for unresolved issues, required permissions or missing input, host-required messages, or your request for status.

Concepts that need no new images proceed directly to production after approval.

## What you receive

| Selection | Final videos |
| --- | --- |
| Lyric video | Two matching exports: one with lyrics and one without lyrics. Both include the original audio. |
| Visualizer | One audio-responsive video without lyrics. |

The workflow also calls for the editable Remotion project, required assets, and reproducible render instructions.

Unless you specify otherwise, the defaults are the full supplied track, 1920 × 1080, 16:9, 30 fps, and H.264 MP4 with AAC audio.

## Lyric timing

AI has difficulty aligning words precisely with sung audio. Lyric videos require multiple timing retries and review passes; an initial transcription or alignment should not be treated as final. Providing accurate lyrics can help with the words, but their timing still needs to be verified against your recording.

If a word or timing ambiguity cannot be resolved, the agent should ask for targeted input rather than invent lyrics or claim precise alignment.

## Requirements

Use an agent that can work with project files, analyze audio, and build and render a Remotion project. The necessary runtime, dependencies, and rendering tools must be available or installable with permission.

Image-generation tools are optional. Their availability depends on your agent and session; automatic generation is offered only when a suitable callable tool is available. Otherwise, use the manual image workflow or agree on a concept using procedural graphics.

Supply audio and assets you have permission to use. Keep fonts and external assets appropriately licensed.

## Repository contents

- [mp3_to_remotionvideo.md](mp3_to_remotionvideo.md) — the complete, self-contained production instructions.
- [README.md](README.md) — this usage guide.

The instructions describe the intended workflow. Output quality and verification capabilities depend on the agent, available tools, and supplied material.
