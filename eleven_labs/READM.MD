## Eleven Labs + Live Avatar Module

This module enables **live interactive interviews** using avatar-based agents. It integrates Eleven Labs' text-to-speech (TTS) and real-time avatar rendering to create a natural, conversational experience. Below is a breakdown of the key files and their purposes:

| File / Folder | Purpose |
|---------------|---------|
| `eleven_labs/cooked/liveavatar-web-sdk/` | The main Live Avatar SDK directory. Contains all frontend and backend code to render avatars, animate lip-sync, and handle speech synthesis. |
| `apps/demo/` | A demo application showcasing how to run a live avatar session. It provides example components for initializing an avatar, starting/stopping a session, and rendering interview dialogues. |
| `src/components/LiveAvatarSession_*.tsx` | React components that handle individual live avatar sessions. Each file may represent a snapshot of session behavior, UI elements, or experimental features. |
| `src/components/interview_*.tsx` | Components specifically designed for managing live interview workflows with avatars, including question-answer interactions and real-time audio playback. |
| `api/start-session/route_*.ts` | API routes for starting and managing avatar sessions. These endpoints handle session creation, user input, and speech synthesis requests. |
| `.history/` | Auto-saved development history of the Live Avatar SDK. These files are typically ignored from Git commits. |
| `package-lock.json` | Locks the dependency versions for Node.js packages used in the Live Avatar SDK. |
| `.vscode/settings.json` | Local VSCode workspace settings for the project (e.g., formatting rules). |
| `tavily_mcp_server.py` (if integrated) | Can be used to query external information during live interviews or feed the avatar contextual knowledge. |

### Purpose

The Eleven Labs + Live Avatar module allows you to:

- Conduct **real-time interviews** with AI avatars.
- Synthesize speech using Eleven Labs TTS.
- Render lip-synced avatars in a browser using the Live Avatar SDK.
- Integrate with SpoonOS agents for dynamic, context-aware interactions.
- Experiment with multiple avatars or session types using the demo components.

> **Tip:** Keep `.env` files out of Git commits, as they contain sensitive API keys for Eleven Labs or other services.

