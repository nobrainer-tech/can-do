# Pochodzenie i pewność

Sprawdzono: **2026-10-31**. Zakres: zasady pracy Claude Code i ich autorska
adaptacja do Codexa. Skill nie zawiera pełnych promptów, prywatnych instrukcji
sesji ani konfiguracji cudzego środowiska.

## Co rzeczywiście zweryfikowano

| Źródło | Wersja i data | Co potwierdza |
|---|---|---|
| Oficjalna paczka Anthropic w npm, `@anthropic-ai/claude-code-darwin-arm64` | 2.1.316, odczyt 2026-10-31 | Obecność bloków pełnego wykonania, autonomii i kontroli zakończenia oraz rozgałęzień dla Fable 5.1 i Opus 5.5. |
| Publiczne zrzuty asgeirtj | commit `ace0f2ccd4e566b5da210a3ed22ef1cfc448663e`, aktualizacja 2026-10-27 opisana jako Claude Code 2.1.312 | Treść opublikowanej pary Fable/Opus. Autorstwo i etykiety pochodzą od autora repozytorium, nie od Anthropic. |
| Wydzielone bloki Piebald | commit `f6aed7fdc41a79d6a8e2e0879998f13029663314`, zbiór dla 2.1.316 | Ułatwiają wskazanie konkretnych fragmentów. Są niezależnym opracowaniem, nie oficjalnym eksportem sesji. |

Oficjalne źródła:

- [Wydanie Claude Code 2.1.316](https://github.com/anthropics/claude-code/releases/tag/v2.1.316).
- [Metadane oficjalnej paczki](https://registry.npmjs.org/@anthropic-ai/claude-code-darwin-arm64/2.1.316).
- [Paczka tej wersji](https://registry.npmjs.org/@anthropic-ai/claude-code-darwin-arm64/-/claude-code-darwin-arm64-2.1.316.tgz).

W badaniu zgodność pobranego archiwum sprawdzono z polem npm `dist.integrity`
przez SHA-512. Archiwum i program analizowano w pamięci, bez wykonania kodu.
Odczytano teksty bloków i warunki ich doboru. To dowód obecności w wydaniu,
nie dowód ich aktywacji w każdej sesji. Konfiguracja i ustawienia usługi
mogą zmieniać złożony zestaw instrukcji.

Publiczne zrzuty i fragmenty:

- [Fable 5.1, przypięty zrzut Claude Code](https://github.com/asgeirtj/system_prompts_leaks/blob/ace0f2ccd4e566b5da210a3ed22ef1cfc448663e/Anthropic/claude-code/claude-code-fable-5.1.md).
- [Opus 5.5, zrzut z tego samego commita](https://github.com/asgeirtj/system_prompts_leaks/blob/ace0f2ccd4e566b5da210a3ed22ef1cfc448663e/Anthropic/claude-code/claude-code-opus-5.5.md).
- [Piebald: Delivering work](https://github.com/Piebald-AI/claude-code-system-prompts/blob/f6aed7fdc41a79d6a8e2e0879998f13029663314/system-prompts/system-prompt-delivering-work-at-full-scope.md).
- [Piebald: Writing for the user](https://github.com/Piebald-AI/claude-code-system-prompts/blob/f6aed7fdc41a79d6a8e2e0879998f13029663314/system-prompts/system-prompt-writing-for-the-user.md).

Pola `ccVersion` poszczególnych fragmentów Piebald wskazują odpowiednio
2.1.218 i 2.1.247. Nie są datą całego odczytanego zbioru ani dowodem,
że fragment wprowadzono dopiero w Fable 5.1.

## Granice wniosków

W tej parze zrzutów Fable zawiera dodatkowy blok pełnego zakresu oraz
bardziej szczegółową kontrolę autonomii i zakończenia. Oba zawierają
zachętę do działania przy wystarczających informacjach. Różnica tekstów
nie dowodzi różnicy skuteczności modeli ani wyłączności zasad dla Fable.
Nie odtworzono pełnych promptów wysłanych w konkretnych sesjach właściciela.

Oficjalne strony promptów
[Opus 5.5](https://platform.claude.com/docs/en/release-notes/system-prompts/claude-opus-5-5)
i [Fable 5.1](https://platform.claude.com/docs/en/release-notes/system-prompts/claude-fable-5-1)
dotyczą czatu Claude. W odczycie najnowsze wpisy miały daty 2026-10-27
i 2026-10-30. Nie zastępują promptów Claude Code.

## Decyzje adaptacji

Zachowano pełny zakres, rutynową samodzielność, wykonanie niezależnych
części i kontrolę faktycznego zakończenia. Dodano praktyczny odbiór wyniku.
Pominięto założenie nieobecności użytkownika, narzędzia Claude, sztywne
ograniczenia stylu i preferencję Bash. Pozostają bieżące reguły Codexa,
upoważnienia właściciela i dostępność narzędzi.

To oznaczona synteza źródeł, nie oficjalny prompt Anthropic. Przy pytaniu
o „najnowszy prompt” sprawdź ponownie wydanie, daty i warunki doboru;
nie przesuwaj daty tej notatki bez ponownej weryfikacji.
