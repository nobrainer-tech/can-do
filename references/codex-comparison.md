# Fable 5.1 i publiczne instrukcje Codexa

Sprawdzono: **2026-10-31**. Codex ma już mocne instrukcje proaktywnego
wykonania. Nie ma podstaw, aby przedstawiać tę adaptację jako wypełnienie
całkowitego braku autonomii w jego prompcie.

## Dokładny materiał porównania

- Fable: para zrzutów Claude Code 2.1.312 i potwierdzenie obecności
  wybranych bloków w oficjalnej paczce 2.1.316, opisane w [sources.md](sources.md).
- Codex: oficjalne repozytorium `openai/codex`, tag **rust-v0.163.0**,
  zgodny z odczytaną lokalną wersją CLI. Podstawą jest
  [models-manager/models.json](https://github.com/openai/codex/blob/rust-v0.163.0/codex-rs/models-manager/models.json),
  rekord `slug: gpt-6.1-sol`, pole `model_messages.instructions_template`.
  Rekord `gpt-6-astra` zawiera te same główne sekcje autonomii.
- W repo pozostają także starsze pliki, np.
  [gpt_5_2_prompt.md](https://github.com/openai/codex/blob/rust-v0.163.0/codex-rs/core/gpt_5_2_prompt.md)
  i [gpt-5.2-codex_prompt.md](https://github.com/openai/codex/blob/rust-v0.163.0/codex-rs/core/gpt-5.2-codex_prompt.md).
  Samo znalezienie ich nazw nie ustala instrukcji współczesnego modelu.

## Porównanie zasad

Poniżej „Codex” oznacza opisany publiczny szablon Sol, a „Fable” opisany zrzut.

| Obszar | Fable | Codex | Wkład skilla |
|---|---|---|---|
| Wykonanie całego zadania | Osobny blok pełnego zakresu. | Sekcja autonomii wymaga doprowadzenia zlecenia do końca. | Krótka kontrola wszystkich warunków odbioru. |
| Zbędne pytania | Samodzielne kroki odwracalne. | Sekcja zgód każe korzystać z wcześniejszych upoważnień. | Przypomnienie, bez nowej kategorii uprawnień. |
| Niejasności | Najpierw niezależne części. | Dalsza praca równolegle z wyjaśnianiem. | Jawne rozdzielenie założenia i blokady. |
| Zakończenie | Kontrola, czy ostatni akapit tylko obiecuje pracę. | Zakaz kończenia na planie lub częściowym wyniku. | Konkretny punkt kontroli przed odpowiedzią. |
| Komunikacja | Samodzielnie zrozumiała odpowiedź końcowa. | To samo, plus zasady aktualizacji postępów. | Zwięzły wynik, dowód i ważne braki. |

Odniesienia w publicznym szablonie: `When to ask the user for permission`,
`Autonomy and persistence`, `Working with the user`, `Intermediate commentary`
oraz `Technical communication`. W katalogu jest także oddzielne pole
`persistent_instructions`; jego obecność nie dowodzi, że tryb został włączony.

## Wniosek i granice

Różnica w codziennym zachowaniu może wynikać z modelu, efektywnego zestawu
instrukcji, narzędzi i stanu kontekstu. To hipotezy, nie zdiagnozowana przyczyna.
Ten skill porządkuje wybrane zasady w jednym wywołaniu; poprawa skuteczności
wymaga porównania rzeczywistych zadań z włączonym i wyłączonym skillem.

Nie potwierdzono, że aktywny Desktop wysyła dokładnie ten publiczny szablon.
Nie eksportowano prywatnego promptu sesji. Skill nie zastępuje globalnych
instrukcji ani nie nadaje nowych możliwości aplikacji.

Mechanizm `model_instructions_file` w
[schemacie tej wersji](https://github.com/openai/codex/blob/rust-v0.163.0/codex-rs/core/config.schema.json)
służy do podmiany bazowych instrukcji i zawiera ostrzeżenie o możliwym
pogorszeniu działania. Nie jest potrzebny do używania tego skilla.
