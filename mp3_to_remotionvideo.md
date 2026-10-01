---
name: audio-to-motion-video
description: Use when a user supplies audio and wants a polished Remotion lyric video or visualizer. Ask for the video type, pitch exactly three concepts for approval, check available image-generation tools, offer automatic or manual image creation, then build, verify, and export. Lyric mode exports matching versions with and without lyrics.
---

# Audio to Motion Video

Create an original, showreel-quality motion piece driven by the supplied recording. Own production from analysis through verified exports. Use the user's aesthetic direction and existing project when supplied. Do not require a fixed genre, brand, or aspect ratio.

This file is self-contained: all workflow and production guidance is included below. Use it as an agent skill or reusable instructions in an agent with access to audio analysis, project files, and Remotion rendering. Image-generation tools are optional; discover what the current agent actually has rather than assuming tools from another platform are available.

## 1. Choose the video type before pitching concepts

Before presenting concepts or beginning lyric transcription, ask:

> Would you like a lyric video or a visualizer without lyrics? AI has difficulty aligning lyrics precisely with sung audio, so lyric timing will take multiple retries and review passes. If you choose a lyric video, I will export two matching videos: one with lyrics and one without, so you can choose which to use.

Wait for the user's selection. If the conversation already clearly specifies the video type, honor it without asking again; still give the lyric-timing reminder before lyric production when applicable.

- **Lyric video:** Analyze and verify the sung words and their timing. Plan two final exports using the same audio, duration, visual design, motion, and render settings: one with the lyric layer enabled and one with it disabled. The version without lyrics must remain visually complete, with no empty lyric placeholders. The user does not need to request the second export separately.
- **Visualizer:** Build audio-responsive visuals without displaying lyrics. Do not require lyric transcription or alignment. Export one final video without lyrics.

If lyric mode is selected but the recording has no sung lyrics, explain the issue and resolve the video type with the user before pitching concepts. Do not invent lyrics.

## 2. Input and discovery

1. Identify the actual audio file, its location, duration, channels, sample rate, and safe working copy. Accept common audio formats, including MP3. If the file is missing, ask for it; do not invent its sound or lyrics.
2. Ask only for missing choices that materially affect the work, such as intended aspect ratio or full track versus excerpt. When unspecified, use a 16:9 composition at 1920×1080, 30 fps and the full supplied track. State these assumptions in the pitch.
3. Listen to the audio, inspect the waveform and musical structure, and note key transitions, vocal entries, repeated hooks, quiet spaces, accents, and ending. Use available audio tools. If a needed binary or package is absent, install it only when permitted and practical; otherwise explain the exact blocker.
4. For lyric mode only, extract lyrics from this recording with timestamps. Prefer word-level or phrase-level transcription with an audio-capable tool or speech recognizer. Preserve uncertainty flags; verify the words by listening at normal and slowed speed. Do not substitute internet lyrics for what is actually sung. User-supplied lyrics can help establish the words, but their timing must still be checked against this recording. Keep the transcript internal until needed for the pitch; do not publish an entire copyrighted lyric transcription in chat unless the user supplied the lyrics or asks for it.
5. Keep a beat/section map in the project. For lyric mode, also keep a timing document with line/word intervals and confidence or uncertainty notes. Make timing monotonic and bounded by the real recording length.

## 3. Three-concept approval gate

After the video type is settled and the audio is analyzed, present **exactly three** genuinely different concepts tailored to the selected type and this recording. Each pitch must include:

- A memorable title and one-sentence visual premise.
- Art direction: palette, type style where relevant, image or shape language, space, and texture.
- Motion language: camera, transitions, rhythm, and how movement responds to the audio.
- For lyric mode, a lyric treatment and how the matching version without lyrics will stand on its own. Use at most a short lyric fragment as an example when useful.
- For visualizer mode, the audio-reactive treatment and focal points, without a lyric layer.
- One signature moment tied to a specific audible event or timestamp.
- A practical production note describing required images, other assets, and techniques. Identify concepts that need no generated images.
- Expected exports: two matching videos in lyric mode, or one video in visualizer mode.

Give a concise recommendation based on the recording and selected video type. Avoid three palette variants of the same template. Make the ideas achievable in Remotion and worthy of a professional motion-design reel: strong hierarchy, memorable visual system, choreographed timing, coherent transitions, and restraint between high-impact moments.

**Stop here and seek the user's explicit choice of concept 1, 2, or 3.** A refinement request counts as approval only when it clearly selects a concept. Do not begin the final composition, full render, or image generation before approval. Audio analysis, lyric work in lyric mode, beat mapping, and lightweight non-generated concept frames or short tests needed to make pitches reviewable are allowed. If a concept is already approved in the conversation, continue without asking again.

## 4. Check image tools and choose the asset workflow

After concept approval, prepare an asset list and inspect the current agent's exposed tools, tool discovery, and applicable permissions to determine whether a callable image-generation tool is actually available. For example, an agent running in Codex may have image-generation tools, but do not assume that every Codex session or other agent has them. An image search tool is not an image-generation tool. Do not claim availability based only on the platform name or these instructions.

If the approved concept needs images:

- **If image generation is available:** Briefly identify the available capability and ask whether the user wants the agent to generate the images automatically with those tools, or wants to generate them themselves using prompts supplied by the agent. Wait for the selection unless the user has already explicitly chosen an available route.
- **If image generation is unavailable:** Explain that automatic image generation is unavailable in this session and provide the manual prompts and upload instructions below. Do not offer automatic generation as an available choice. If the user cannot supply images, resolve an alternative with them, such as a revision of the approved concept using procedural graphics.
- **If no new images are needed:** State this in the concept pitch. Once approved, proceed directly to production using the approved procedural or already supplied assets; do not introduce an unnecessary image-choice gate.

Do not change the approved art direction simply to avoid a tool limitation without the user's agreement.

### Automatic images

Once the user chooses automatic image generation, begin immediately. Generate every required image using the available tools and validate it against the approved concept and asset constraints. Retry generation or repair unsuitable images without requesting routine approvals. Follow the tool's actual requirements and respect any required permissions.

Continue through composition, internal draft review, corrections, full rendering, and verification of all required exports. **Do not send routine progress reports, concept previews, image approval requests, or draft handoffs. Report back when the required final videos are exported and verified.** Interrupt only for an issue that cannot be resolved autonomously, required permission or missing input, or an explicit user request for status. Host-required messages or tool displays may still occur; keep any required messages minimal and do not add optional updates.

### Manual images

Provide a complete, clearly labeled prompt for **each** required image. Include:

- Asset ID and suggested filename, matching its planned scene or use.
- A ready-to-copy generation prompt covering subject, composition, camera, lighting, palette, texture, and style.
- Required aspect ratio, minimum useful pixel dimensions, file format, and transparency when needed.
- Safe areas, negative space for lyric overlays when relevant, crop allowance, and any layering or background requirements.
- Consistency instructions across images, and exclusions such as unwanted text, watermarks, or logos.

Then ask the user to provide all images, labeled with the asset IDs or filenames. Wait for the images; do not fabricate replacements or silently switch to automatic generation.

When images arrive, inspect the actual files and confirm **internally** that they fit the constraints: required assets are present, files are readable, dimensions and aspect ratios are usable, intended crops work, transparency is correct where needed, and art direction and text-safe areas match the approved concept. Correct routine format or crop issues locally when doing so preserves the supplied artwork and approved direction.

If an image is missing or unsuitable and cannot be corrected safely, explain the specific issue and request only the affected replacement or missing asset. Otherwise, proceed immediately without a separate confirmation or approval message. **Do not report back until all required final videos are exported and verified**, subject to the same unresolved-issue, required-permission, host-message, and user-status exceptions as the automatic route.

## 5. Production after approval and asset readiness

1. Write an internal creative brief recording the selected video type, concept, aspect ratio, length, fps, export count, lyric policy, palette, typography, recurring motifs, asset list, and three or more timed hero moments.
2. Build a Remotion project using current official Remotion APIs and local package versions. Keep the editable source project deliverable. Use licensed, user-supplied, or appropriately generated assets and fonts; record their sources in the project. Avoid stock-template aesthetics and irrelevant visual noise.
3. Set composition duration from measured audio duration. Use the source audio as the edit master. Align cuts, impacts, transitions, and lyric cues when applicable in frames; handle sample-to-frame rounding consistently so the end does not drift. Protect text safe areas and readability on mobile-sized previews.
4. In lyric mode, use one shared composition with a lyric-visibility option or equivalent shared implementation. Preserve the same audio, visuals, choreography, duration, and settings in both exports. Disabling lyrics must remove only the lyric overlay and any lyric-only decoration, without leaving gaps or placeholders.
5. Animate with deliberate staging and easing. Prefer a small, consistent motion vocabulary and occasional surprising hero transitions over constant movement. Build depth with typography, masking, shape choreography, lighting, and camera perspective only where they serve the chosen concept. No default fades as a substitute for design. Honor any reduced-flash or accessibility constraint the user gives.
6. Render an internal draft excerpt covering at least one verse or section change and the signature moment. Inspect frames and watch with audio. Fix clipping, collisions, abrupt cuts, timing drift, motion judder, dead frames, and unreadable or mistimed lyrics. In lyric mode, perform multiple timing review and correction passes as needed, checking vocal entries and repeated hooks against the recording. Do not treat an initial AI alignment as final. Keep draft review internal rather than asking the user to approve each retry.
7. Render the complete required output set. Use a high-quality H.264 MP4 with AAC audio unless the user requests another format. Suggested names: `<track>-with-lyrics.mp4` and `<track>-without-lyrics.mp4` in lyric mode; `<track>-visualizer.mp4` in visualizer mode. Both lyric-mode exports include the original audio; without lyrics does not mean silent.
8. Verify **each** export exists, decodes and plays, has the expected dimensions, fps, duration, and audio, and has no truncated ending. Inspect beginning, middle, ending, and transition samples. In lyric mode, verify that lyrics are present only in the designated version and that the version without lyrics stands on its own. Fix rendering failures and retry; do not call a failed or uninspected file finished. If tools cannot support a necessary verification, report that limitation rather than claiming the check passed.
9. Deliver all required final videos together, the editable Remotion source and required assets, and a short note identifying the selected concept and any remaining limitation. Give direct file links. In lyric mode, label both exports clearly so the user can choose either. Do not deliver just one lyric-mode export as a completed job.

## Production notes and craft checks

### Timing artifacts

Store a machine-readable timing file with audio duration, detected sections, and beat accents. In lyric mode, include cues with `start`, `end`, `text`, and verification status. Use seconds for source timing and convert to integer frames at the render boundary. Word-level timing suits kinetic typography; carefully checked phrase-level timing is acceptable. Check overlaps, negative intervals, missing gaps, and cues beyond the track. Resolve or omit uncertain words; never fabricate them. If a necessary lyric or timing ambiguity cannot be resolved, request targeted input instead of claiming precise alignment.

### Concept differentiation

Make the three proposals vary along several axes: physical versus graphic material, intimate versus monumental camera scale, sparse versus layered composition, and smooth versus percussive choreography. Each concept should suggest specific scenes for this audio and the chosen video type, not a generic mood board.

### Design review

The visuals must clearly respond to this track's structure and accents, and to its verified lyrics in lyric mode. At thumbnail size, the focal point and any lyric hierarchy must read. At full size, shapes, masks, and type should have clean edges. Text contrast and dwell time must support reading; avoid long lyric paragraphs. Give the eye a place to rest before high-energy changes. Check flashes and rapid contrast changes, especially around beat impacts. Preserve audio without accidental gain changes or added distortion. Build an opening hook, evolving middle, strong payoff, and intentional final frame. The result should hold up without sound while feeling synchronized when audio plays.

### Reproducible handoff

Keep working files organized. Document exact render commands for every output variant, dependency versions, dimensions, fps, source-audio filename, and asset sources in the delivered project's README. Preserve the editable source and required local assets. Exclude generated caches and dependency folders from the project handoff. This runtime README belongs to the video project; no separate reference file is required to use this instruction file.
