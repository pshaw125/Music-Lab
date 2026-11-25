# Sounds, effects and assets

The application must be usable offline. Any sound, effect, impulse response or other asset required by a bundled preset must be available locally; no network fetch should be required to play or export a project.

## Initial candidates

- Synthesize pitched sounds where practical: bass, lead, pluck and pad.
- Use either synthesized percussion or a small, carefully sourced collection of drum one-shots.
- Evaluate built-in synthesis and effects in Tone.js, including filter, delay and reverb, during the Mac audio spike. No library or preset is yet approved for inclusion.
- Preset macros may control multiple sound parameters. Record their parameter mappings and ranges as part of the preset so playback is reproducible.

## Asset policy

Track provenance for each bundled asset: source, creator, exact license and version, redistribution rights, attribution, modifications and any relevant restrictions. A code license does not automatically apply to included audio; free downloads are not automatically redistributable. Review the actual terms before importing an asset.

Keep project-authored code, configuration, documentation, preset definitions and appropriate small redistributable assets in Git. Decide how to handle larger or restricted assets individually before adding them: consider Git LFS or a separately distributed, locally installable pack, while preserving offline functionality. Do not commit assets without rights to include them. Record the chosen strategy here when there are real assets to evaluate.

Sound-set names and machine references in other music tools are inspiration, not evidence of a right to copy their assets or presets.
