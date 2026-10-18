# Historical Documentary Video Workflow

Create historically grounded documentaries about **events, people, places, inventions, ideas and buildings**, using a photorealistic presenter introduction followed by animated watercolor scenes.

## Requirements

- A browser-capable agent that can follow the instructions in `SYSTEM_PROMPT.md`.
- Access to [VideoExpress](https://app.videoexpress.ai/), with generation access available. Documentary narration is prepared as text and a voice-direction prompt for the voice app you choose; CloneVoice is not required.
- Sign in when prompted. The workflow uses the agent's visible built-in browser unless you authorize another browser.

This folder contains instructions for browser automation. It is not a standalone executable or a direct API workflow.

## How to use

1. Load `SYSTEM_PROMPT.md` as the instructions for your browser automation agent, or ask the agent to read and follow that file.
2. Start the workflow. It asks four questions together:

   | Question | Default |
   |---|---|
   | Idea/Script | Supply a historical topic or your own script |
   | Character | Daniel Reed, a fictional male presenter with a calm American English voice |
   | Ratio | Landscape 16:9; Vertical 9:16 is also supported |
   | Duration | 60 seconds total, up to 5 minutes |

3. Reply with your choices. For example:

   ```text
   Idea/Script: Explain why Julius Caesar was assassinated and what followed.
   Character: Keep the default.
   Ratio: Landscape.
   Duration: 120 seconds.
   ```

4. Let the agent complete generation and timeline assembly. It saves the project and clicks **Export Video**, then stops. It does not download the video.

## What it creates

**Presenter intro — at least 20 seconds:** A character sheet establishes the presenter. The agent saves it to My AI Images, uses it as a consistent-character reference for a location scene, then generates speaking clips with the same voice description. The intro gives context and introduces the topic's story arc.

**Historical documentary:** The agent provides a narration script and a separate voice-generation prompt for your chosen app. Watercolor-and-ink visuals follow the story arc: context, people and causes, key events or processes, and consequences. Construction details appear when relevant to the subject. Clothing, equipment and architecture follow the period and place.

**Active multi-shot clips:** Prompts use `Total duration` and timed `SHOT 1 / SHOT 2 / SHOT 3` sections, with hard cuts and distinct camera angles. Actions fit the subject: workers build when construction matters; historical figures make decisions, meet, travel, act and react when the story is an event or biography. Asset IDs and internal labels stay out of generation text; subtitles and visible shot labels are not requested.

## Audio and video timing

The requested duration guides the initial script. You generate the narration in your chosen voice app using the supplied text and voice prompt, then provide the finished audio for timeline assembly. The audio is reused unchanged: no repeated generation, audio cuts, silence trimming or speed changes to force a target runtime. Until you provide it, the project is a visual draft.

The narration starts after the actual intro endpoint. Video coverage extends to the audio clip's right edge. To remove excess footage, the agent places the playhead at that edge, selects the last video clip, clicks **Cut**, and deletes only the excess right-hand video chunk. The final length therefore follows the completed audio plus intro and can differ slightly from the initial estimate.

## Working preferences

- No routine audio/video playback QA or unrequested Share actions.
- Presenter speech stays audible; documentary clip audio is muted beneath the separately generated voiceover. Until you supply that audio, the saved project is a visual draft.
- Reuse completed assets when resuming a production.
- Edit instructions in place; do not create timestamped backup prompts or unnecessary reports.
- Generated visuals and voice consistency can vary. Review the saved result before publishing. The narration script and voice direction are supplied for your external voice app.

## Files

- [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) — instructions the automation agent follows.
- `README.md` — this short usage guide.


