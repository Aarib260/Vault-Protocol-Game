# Graph Report - bank-security-game  (2026-10-31)

## Corpus Check
- cluster-only mode — file stats not available

## Summary
- 155 nodes · 310 edges · 9 communities
- Extraction: 97% EXTRACTED · 3% INFERRED · 0% AMBIGUOUS · INFERRED: 9 edges (avg confidence: 0.87)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Project setup & dependencies
- Gemma API client & error handling
- Scoring rules & constants
- Express server, routes & sessions
- Frontend: chat, typing, meter, overlays
- README docs
- Turn referee (applyTurn)
- Story data: stages, intel, questions
- Tone detection (sir / rude)

## God Nodes (most connected - your core abstractions)
1. `send()` - 22 edges
2. `🔓 Vault Protocol` - 15 edges
3. `applyTurn()` - 14 edges
4. `renderAll()` - 13 edges
5. `createApp()` - 12 edges
6. `el()` - 9 edges
7. `restart()` - 9 edges
8. `typeMessage()` - 9 edges
9. `InvalidAiResponseError` - 7 edges
10. `validateAiResponse()` - 7 edges

## Surprising Connections (you probably didn't know these)
- `🛠️ Customise it` --references--> `buildSystemPrompt()`  [INFERRED]
  README.md → server/prompts.js
- `🛠️ Customise it` --references--> `typeMessage()`  [INFERRED]
  README.md → public/script.js
- `withServer()` --calls--> `createApp()`  [EXTRACTED]
  test/game.test.js → server/index.js
- `turn()` --calls--> `applyTurn()`  [EXTRACTED]
  test/game.test.js → server/gameLogic.js
- `turn()` --calls--> `validateAiResponse()`  [EXTRACTED]
  test/game.test.js → server/gameLogic.js

## Import Cycles
- None detected.

## Communities (9 total, 0 thin omitted)

### Community 0 - "Project setup & dependencies"
Cohesion: 0.10
Nodes (21): dependencies, dotenv@^16.4.5, express@^4.21.2, @google/genai@^2.32.0, description, engines, node, keywords (+13 more)

### Community 1 - "Gemma API client & error handling"
Cohesion: 0.15
Nodes (13): createGameState(), InvalidAiResponseError, parseAiJson(), assertGemmaModel(), createGemmaClient(), GemmaError, generateTurnWith(), toGemmaError() (+5 more)

### Community 2 - "Scoring rules & constants"
Cohesion: 0.11
Nodes (17): cleanString(), CORRECT_ANSWER_CHANGE, FORMAL_MARKERS, goalsFor(), INTERJECTIONS, KEYBOARD_ROWS, looksLikeGibberishWord(), MAX_MESSAGE_LENGTH (+9 more)

### Community 3 - "Express server, routes & sessions"
Cohesion: 0.21
Nodes (11): createSessionStore(), isUnintelligible(), nextQuestionKind(), publicState(), stage1TranscriptText(), validateAiResponse(), validatePlayerMessage(), createApp() (+3 more)

### Community 4 - "Frontend: chat, typing, meter, overlays"
Cohesion: 0.15
Nodes (33): addDivider(), addMessage(), addSystem(), api(), autoResize(), clearError(), el(), hideOverlay() (+25 more)

### Community 5 - "README docs"
Cohesion: 0.11
Nodes (18): API routes, 🙏 Credits, 🌍 Deploy it (free, with Render), ✨ Features, 🏗️ How it works, 🎮 How to play, 🔭 Ideas for later, ⚠️ Known limitations (+10 more)

### Community 6 - "Turn referee (applyTurn)"
Cohesion: 0.22
Nodes (9): applyTurn(), claimsManagerSent(), clamp(), isDifferentName(), lastQuestion(), norm(), pick(), setPending() (+1 more)

### Community 7 - "Story data: stages, intel, questions"
Cohesion: 0.25
Nodes (7): BRIEFING, BRIEFING_QUESTIONS, DOSSIER, FALLBACK_QUESTIONS, JSON_REPAIR_INSTRUCTION, STAGES, UNINTELLIGIBLE_REPLIES

### Community 11 - "Tone detection (sir / rude)"
Cohesion: 0.67
Nodes (3): decideTone(), formalScore(), rudeScore()

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `🛠️ Customise it` connect `Frontend: chat, typing, meter, overlays` to `Express server, routes & sessions`, `README docs`?**
  _High betweenness centrality (0.520) - this node is a cross-community bridge._
- **Should `Project setup & dependencies` be split into smaller, more focused modules?**
  _Cohesion score 0.1038961038961039 - nodes in this community are weakly interconnected._
- **Why does `buildSystemPrompt()` connect `Express server, routes & sessions` to `Gemma API client & error handling`, `Frontend: chat, typing, meter, overlays`, `Story data: stages, intel, questions`?**
  _High betweenness centrality (0.466) - this node is a cross-community bridge._
- **Should `Scoring rules & constants` be split into smaller, more focused modules?**
  _Cohesion score 0.10526315789473684 - nodes in this community are weakly interconnected._
- **Should `README docs` be split into smaller, more focused modules?**
  _Cohesion score 0.10526315789473684 - nodes in this community are weakly interconnected._