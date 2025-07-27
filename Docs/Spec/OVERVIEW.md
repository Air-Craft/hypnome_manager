Spec: AI-Guided Hypnosis Journey App
Name : Hypnome

REPO: git@github.com:Air-Craft/hypnome.git

OVERVIEW
A fully voice-driven experience where the user shares a desire aloud, and the AI guides them through a personalized hypnosis journey to reprogram their inner messaging. The app interviews the user, intuitively selects an induction method, delivers a custom hypnotic script (using Eriksonian techniques), gives time for subconscious integration, and then gently returns them to full awareness. The whole session is backed by ElevenLabs voice synthesis enhanced with SSML for nuanced pacing and tone, and includes optional background music. The interface should have minimal UI driven by voice (STT and TTS) and be similar to voice mode in Open AI's app. 

STAGE 1: VOICE INPUT + INTERVIEW
Purpose:
Gather the user’s intent, emotional context, and symbolic/imaginal data to shape the hypnosis session.
Interface:
* The user initiates by tapping a microphone button, modeled on ChatGPT’s voice UI.
* They speak freely about what they want to change, work on, or become.
* The app transcribes the spoken content using a tool like Whisper or similar.
Interview:
* AI follows up with 2–4 voice questions.
* Prompts are generated dynamically based on tone and content. Example questions:
    * “When you imagine that outcome, what kind of energy or imagery comes to mind?”
    * “What seems to get in your way, either internally or externally?”
    * “If this desire had a voice, what would it say?”
* The tone remains soft, reflective, and empathetic.
Output:
* Structured transcription (intent, emotions, key symbols).
* Internal belief flags.
* Temperament markers to assist with method selection.

STAGE 2: INDUCTION METHOD SELECTION + DELIVERY
Purpose:
Ease the user into a receptive, suggestible state.
Induction Method Selection:
AI chooses the best method based on temperament, emotional cues, and language. Available Induction Styles:
1. Progressive Relaxation – slow body scan, muscle release.
2. Ericksonian Induction – permissive, story-based, indirect suggestions.
3. Visualization – guide to a calming inner world or symbolic transformation.
4. Metaphor – abstract symbolic narrative that mirrors the user’s situation.
5. Reframing – gentle shift in interpretation of belief or memory.
6. Double-Bind – structured choice that leads to the same end (e.g., “As you listen to my voice… or as you relax even deeper…”).
7. Confusion Induction – bypassing logic through subtle pattern interrupt or paradox.
8. Focal Point Induction – user is directed to focus on a sound, breath, or mental image.
Voice Tech:
* Induction script is spoken using ElevenLabs, with SSML controlling:
    * Slow pacing
    * Pauses (<break time="1s"/>)
    * Emphasis tags
    * Gentle shifts in tone (whisper, softness, authority)
    * Embedded hypnotic cues

STAGE 3: HYPNOSIS SCRIPT DELIVERY
Purpose:
Deliver the core transformation.
Content Generation:
* Script built around:
    * The user’s stated desire
    * Symbolic language they used (e.g., “a wall around my heart” becomes a metaphor)
    *
    * Positive reprogramming
    * Present-tense reinforcement
* Techniques used:
    * Affirmations (subtle, embedded)
    * Future pacing (e.g., “as you move through tomorrow…”)
    * Double-binds for compliance
    * Reframing stuck beliefs
    * Metaphoric transformation scenes
    * Subliminal suggestion embedding (soft emphasis on action phrases)
Voice Tech:
* Delivered via ElevenLabs using SSML for all nuance.

STAGE 4: PERCOLATION SPACE (SUBCONSCIOUS INTEGRATION)
Purpose:
Let the user’s system quietly absorb the work.
Mechanism:
* 5-minute timer
* Ambient music plays softly during this phase
Music:
* Default track: Jamendo – “Still and Floating”
* May add fade-in and fade-out SSML style pacing or sound overlay depending on implementation method
Optional Features:
* Visual cue (e.g., pulsing dot)
* Option to skip percolation for advanced users

STAGE 5: RETURN + CLOSING
Purpose:
Guide the user gently back to waking awareness.
Process:
* Spoken by ElevenLabs voice
* Gradual awakening process (e.g., breath cues, counting up from 1 to 5)
* Final positive reinforcement (e.g., “You bring back only what’s useful, and leave behind what no longer serves.”)
Optional:
* “How do you feel now?” check-in
* Reminder to journal, reflect, or revisit later

TECH STACK
Frontend: iOS Native
Backend: Node.js with Typescript
Voice Synthesis:	ElevenLabs + SSML
Backend AI Logic: Using Langchain (Use OpenAI ChatGPT API for now)
Music Hosting	Direct streaming from Jamendo or local embed
