# Decision #0003

## Title

Motion Intelligence Foundation

---

## Status

Accepted

---

## Date

2026-06-23

---

# Context

Pe măsură ce Video Engine a evoluat, a devenit evident că logica bazată pe reguli hardcodate (`if/else`) nu poate susține obiectivul pe termen lung al CopyStack.

Video Engine trebuie să poată lua decizii inteligente, să fie ușor de extins și să poată explica de ce a ales un anumit efect sau o anumită mișcare.

În plus, aceeași infrastructură trebuie să fie reutilizată ulterior de Explain Mode și de aplicația Localhost.

---

# Decision

Motion Intelligence va fi construit pe trei componente independente:

1. Motion Decision Engine
2. Motion Recipe System
3. Motion Plugin System

Rendererul nu conține logică de decizie.

Rendererul execută exclusiv instrucțiunile generate de Motion Decision Engine.

---

# Architecture

Speech Analysis
↓
Story Engine
↓
Timeline Planner
↓
Motion Decision Engine
↓
Motion Recipes
↓
Motion Plugins
↓
Motion Renderer
↓
FFmpeg

---

# Principles

## AI decides

Toate deciziile sunt luate înainte de etapa de randare.

---

## Renderer executes

Rendererul nu decide.

Rendererul execută doar instrucțiunile primite.

---

## Recipes define behavior

Comportamentul Motion Intelligence este descris prin rețete reutilizabile și configurabile.

---

## Plugins implement effects

Fiecare efect este implementat ca un plugin independent.

---

## Story influences motion

Motion-ul nu este determinat doar de transcript sau audio.

Acesta trebuie să țină cont și de progresul narativ al videoclipului.

---

## Explainability

Fiecare decizie trebuie să poată fi explicată prin:

- recipe_id
- recipe_name
- confidence
- reason

Aceste informații vor fi utilizate de Explain Mode.

---

# Consequences

## Advantages

- arhitectură modulară
- extensibilitate ridicată
- testare independentă
- integrare ușoară cu Localhost
- compatibilitate cu Explain Mode
- posibilitatea introducerii unor modele AI mai avansate fără modificarea rendererului

---

## Trade-offs

- număr mai mare de componente
- complexitate inițială mai ridicată
- necesitatea unei documentații mai detaliate

Aceste compromisuri sunt acceptate deoarece oferă o bază solidă pentru dezvoltarea pe termen lung.

---

# Future Impact

Această decizie reprezintă fundația tuturor dezvoltărilor viitoare din zona Motion Intelligence.

Noile animații, efecte și reguli de editare vor fi adăugate prin Recipes și Plugins, fără modificarea Motion Renderer-ului.

Această arhitectură permite integrarea viitoare cu:

- Explain Mode
- Asset Library
- Research Center
- Localhost
- viitorii AI Employees din ecosistemul CopyStack

---

# Approved

2026-06-23
