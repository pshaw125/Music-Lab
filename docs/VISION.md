# Project vision

## Idea

Make electronic music by combining musical ideas at a comfortable level of detail. A beginner should be able to assemble a satisfying piece without writing code or designing a synthesizer. A curious musician should eventually be able to open up the parts, change patterns and shape the sound.

Inspiration includes Figure's immediacy, Punk-o-matic's assembly of parts into a song, and Strudel's composability, with a more guided interface and a different aesthetic. The application itself does not require or include an active AI component.

Tactile interaction is central: sliders, knobs and switches should invite experimentation, like a synthesizer or effects pedal. A preset may expose one or two expressive macro controls—a kind of cooking dial—that coordinate multiple parameters. Eventually those controls can be opened up into their constituent parameters. The exact behavior of each macro is preset-specific and should be understandable through listening and clear labeling.

## Levels of detail

1. **Song and arrangement:** compose sections spanning multiple channels into a song.
2. **Part:** assemble and vary a single-channel musical idea using presets, key, chords and progressions; chain patterns into riffs.
3. **Pattern:** construct musical building blocks by specifying notes and rhythm. The notation and editing experience remain open design work.
4. **Sound:** control synthesis and effects, such as oscillator, envelope, filter and reverb. This is the last feature layer to flesh out.

These are levels of user control, not necessarily separate screens. A preset part combines a sound and musical material so it can be used immediately. The model should distinguish the sound, pattern, part, section and song to support recombination later. Exact vocabulary and boundaries remain open to revision.

## Musical defaults

- Projects have a tempo and key. Scale-relative pitched material adapts when the key changes; drums do not. Chord progressions can be expressed relative to the key.
- Chromatic notes and different interpretations of pitch may be supported later. Store the interpretation explicitly rather than assuming bare numbers mean semitones or scale degrees.
- Pitch and rhythm are separate concepts. Notes need timing and duration as well as pitch; the notation, rhythmic resolution and editing interactions are not yet decided.
- Music theory can inform intelligent defaults without preventing future flexibility. The owner has practical theory knowledge and wants to explore the balance rather than impose a simplistic theory model.

## Reuse and editing

Parts can be reused by reference. When editing a part, offer two explicit save choices:

1. **Update existing:** update the shared part and propagate changes to its references.
2. **Save as new:** supply a new name and create an independent part. Optionally replace the relevant part reference in the open project with the new part.

The exact scope of the optional replacement—one occurrence, a section, or all references in the current project—needs a clear design before implementation. The interface must make the consequences of shared edits visible. Storage ownership and cross-project sharing also remain open decisions.

## Offline and platforms

The app must work fully offline after installation and availability of its included assets: create, edit, play, save, reopen and export without an account or network. Bundled sounds and effects must not rely on remote services at playback time. Project export provides a backup and transfer path.

Develop and test on Mac first. Desktop and iPhone are intended destinations, but phone development follows the Mac prototype. A web-based application and potential packaging are proposed, subject to feasibility testing; native audio remains an option if needed.

## Initial scope

v0.1 prioritizes **assemble and vary**: select preset parts, adjust accessible controls, chain musical patterns, combine channels into sections and order sections into a song. Editing individual notes and deep sound design are later capabilities; their data needs should inform the model without forcing those editors into v0.1.

Proposed baseline: transport, project tempo and key, a small set of drum/bass/lead/chord presets, per-part volume and mute, reusable sections, local save/reopen, editable project export/import and stereo audio export. Final scope should follow the first playback spike and user feedback.
