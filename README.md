# Wargame Studio

A NATO Wargaming Handbook (HQ SACT, 2023) 18 lépéses folyamatára épülő wargame-alkalmazás.

**Jelenlegi verzió:** demó v0.2 (2026-11-06) – statikus, egyfájlos (`index.html`), böngészőben futó prototípus.

## Mit tud a v0.2
- 18 lépéses életciklus kapukkal (szerepfeladatok, produktum, megbízói pontok, DCAP- és rendezvényszál)
- 4×10 szereplista: minden ülés Ember (QR, mobilnézet) vagy AI (egyedi prompt)
- Játéktér: playtest, főpróba, végrehajtás (injekt, döntés indoklással, elbírálás, közlés)
- DCAP, ODCR, gyorsjelentés
- Sötét/világos téma, procedurális terephátér

## Korlátok
Az állapot csak az adott böngészőben (localStorage) tárolódik; az AI-ülések döntései szimuláltak. Következő: v0.3 – többeszközös szinkron, LLM-bekötés.

## Verziók
`releases/` – a kiadott, verziószámozott és dátumozott példányok.
