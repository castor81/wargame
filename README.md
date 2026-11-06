# Wargame Studio

A NATO Wargaming Handbook (HQ SACT, 2023) 18 lépéses folyamatára épülő wargame-alkalmazás.

**Jelenlegi verzió:** demó v0.2.2 (2026-11-06) – egyfájlos (`index.html`) prototípus, telefonos játékosnézet élő szinkronnal (Supabase), térképes csapatkártyával (hover/koppintás: döntési mátrix + eredmény-diagramok).

## Mit tud a v0.2
- 18 lépéses életciklus kapukkal (szerepfeladatok, produktum, megbízói pontok, DCAP- és rendezvényszál)
- 4×10 szereplista: minden ülés Ember (QR, mobilnézet) vagy AI (egyedi prompt)
- Játéktér: playtest, főpróba, végrehajtás (injekt, döntés indoklással, elbírálás, közlés)
- DCAP, ODCR, gyorsjelentés
- Sötét/világos téma, procedurális terephátér

## Telefonos játékosnézet (v0.2.1)
A gazdagép (host) a játék kompakt állapotát a Supabase `wg_rooms` táblába publikálja (`wg_put_state`), a telefon a QR-ral megnyitott `?room=KÓD&seat=ÜLÉS` címen ezt olvassa (`wg_get_state`), és a döntéseket eseményként küldi vissza (`wg_post_event`), amit a host lekérdez (`wg_poll_events`). A táblák RLS-sel zártak, minden hozzáférés a security definer függvényeken át megy. A szoba a host böngészőjében tárolt kulccsal írható.

## Korlátok
A host teljes állapota a böngészőben (localStorage) tárolódik; az AI-ülések döntései szimuláltak. A Supabase-projekt KM-dev, a táblák `wg_` előtagúak. Következő: v0.3 – LLM-bekötés (n8n), szoba-takarítás, jogosultságok.

## Verziók
`releases/` – a kiadott, verziószámozott és dátumozott példányok.
