# Active work and roadmap

## Current stage: planning and feasibility

**Goal:** establish the product model and validate a small, playable Mac prototype before committing to a larger architecture.

- [x] Capture the vision, layered composition model and offline requirement.
- [x] Record part editing and save-as-new behavior.
- [x] Record expressive tactile controls and preset macros.
- [ ] Initialize Git and make an initial commit once repository metadata is writable.
- [ ] Decide the smallest playback spike and project setup.
- [ ] Compare bundled synth/effect capabilities and audition candidate sounds.
- [ ] Define rhythm representation and the pattern/part boundaries with the project owner.

## Proposed iterations

1. **Mac audio spike:** play a synchronized drum groove and pitched synth riff with tempo and key controls. Test local playback without a network.
2. **Assemble and vary:** choose preset parts and patterns, adjust volume and a small number of tactile macros, and chain patterns into a loop.
3. **Arrange:** combine channels into sections; duplicate, reorder and play sections as a song. Implement explicit shared-part editing and save-as-new semantics when the relevant editing workflow exists.
4. **Preserve and share:** save and reopen locally; import/export a versioned project file and render a stereo audio file offline.
5. **Polish and evaluate:** refine touch-friendly and desktop interactions, sounds and onboarding; decide whether the next iteration should emphasize pattern editing, sound design or phone support.

Milestones are a direction, not a promise that each feature will land in isolation. Keep the smallest end-to-end path playable as the design evolves.

## Proposed technical direction

- TypeScript for application logic and UI, gaining experience relevant to the owner's career interests.
- Web Audio and Tone.js as the first playback candidates; Tonal as a candidate for theory utilities. Validate the libraries, current versions, behavior and licenses before adopting them.
- Separate the versioned project model, musical interpretation, playback planning, audio engine and UI. Schedule audio using the audio clock rather than UI timers.
- Start with Mac; defer iPhone packaging and device-specific work. Keep a backend boundary in mind, but avoid speculative abstractions until a concrete need emerges.

## Open questions

- How should rhythm and rests be represented and edited?
- What are the minimum useful controls on a preset, and what should each macro do?
- Is a part library project-local, shared across projects, or both? What exactly does replacing a reference affect?
- What content and licenses can be bundled, including synth presets, samples, effect impulse responses and dependencies?
- What export format and limits are appropriate for the first release?
- Which desktop packaging strategy, if any, is justified after the Mac spike?
