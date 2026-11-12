AI Knowledge Base

Centralna baza wiedzy, dokumentacji technicznej i standardów dla projektów związanych ze sztuczną inteligencją.

Cel projektu

"AI-KNOWLEDGE-BASE" jest wspólnym centrum wiedzy dla wszystkich projektów AI. Jej zadaniem jest gromadzenie, porządkowanie i aktualizowanie informacji technicznych, architektury systemów, konfiguracji, procedur oraz wniosków z przeprowadzonych testów.

Baza ma zapewniać ciągłość pracy pomiędzy projektami i agentami AI. Informacje zapisane w repozytorium powinny być możliwe do ponownego wykorzystania bez konieczności odtwarzania wcześniejszych rozmów.

Główne założenia

- Jedno centralne repozytorium dla wszystkich projektów AI.
- Dokumentacja przechowywana w GitHub w formacie Markdown i MDX.
- Czytelna witryna dokumentacji publikowana przez Docs7.
- Context7 MCP wykorzystywany do wyszukiwania dokumentacji zewnętrznych bibliotek.
- Manus pełni rolę głównego agenta programistycznego i dokumentacyjnego.
- Zmiany w dokumentacji wymagają zatwierdzenia użytkownika przed publikacją na głównej gałęzi.
- Rozwiązania powinny uwzględniać możliwość pracy lokalnej oraz wykorzystania bezpłatnych zasobów chmurowych, jeśli użytkownik wyrazi na to zgodę.

Architektura systemu

Element| Odpowiedzialność
GitHub| Główne repozytorium i historia zmian
Docs7| Publikacja dokumentacji projektowej
Context7 MCP| Dokumentacja zewnętrznych bibliotek i frameworków
Context7 Admin| Zarządzanie dokumentacją i witrynami Docs7
Manus| Analiza, programowanie i przygotowywanie dokumentacji
Windows| Lokalne środowisko programistyczne i testowe
Kaggle| Opcjonalny zdalny backend GPU, uruchamiany za zgodą użytkownika

Projekty

ComfyUI

Dokumentacja lokalnego środowiska ComfyUI, API, workflow, optymalizacji oraz tworzenia własnych węzłów (custom nodes).

LoRA Training Studio

Dokumentacja powtarzalnego procesu przygotowania danych, treningu, konfiguracji i eksportu modeli LoRA.

GPU Backend

Architektura wykorzystania lokalnej karty graficznej i opcjonalnego zdalnego backendu GPU.

AI Agents

Dokumentacja architektury agentów AI, serwerów MCP, pamięci i systemów RAG oraz integracji narzędzi.

Model zarządzania zmianami — tryb hybrydowy

Wszystkie zmiany w dokumentacji i kodzie podlegają następującemu procesowi:

1. Analiza — agent sprawdza istniejące pliki, strukturę projektu i dostępne źródła.
2. Przygotowanie — agent tworzy propozycję zmian w osobnej gałęzi lub wersji roboczej.
3. Weryfikacja — agent sprawdza poprawność, spójność i kompletność przygotowanych materiałów.
4. Zatwierdzenie — użytkownik przegląda zmiany i podejmuje decyzję o ich przyjęciu.
5. Publikacja — dopiero zatwierdzone zmiany mogą zostać scalone z "master".
6. Aktualizacja Docs7 — witryna dokumentacji pobiera zatwierdzoną wersję z repozytorium.

Agent nie może samodzielnie omijać etapu zatwierdzenia.

Zasady dokumentowania

Każda dokumentacja techniczna powinna, zależnie od tematu, zawierać:

- Cel i zakres rozwiązania.
- Architekturę i zależności.
- Wymagania środowiskowe.
- Instrukcję instalacji i konfiguracji.
- Przykłady użycia.
- Procedurę testowania.
- Znane ograniczenia i problemy.
- Informacje o wersjach i źródłach.

Nie należy przedstawiać nieprzetestowanych rozwiązań jako działających. Należy rozróżniać informacje potwierdzone, propozycje i kwestie wymagające sprawdzenia.

Bezpieczeństwo

- Nie zapisujemy kluczy API, tokenów, haseł ani innych sekretów w repozytorium.
- Pliki ".env" i lokalne konfiguracje zawierające dane dostępowe muszą być wykluczone z Git.
- Operacje publikacji, usuwania i zmiany uprawnień wymagają zgody użytkownika.
- Kaggle i inne zewnętrzne zasoby obliczeniowe mogą być wykorzystywane wyłącznie zgodnie z decyzją użytkownika.
- Agent nie może zmieniać założeń projektu ani podejmować decyzji dotyczących kosztów bez zgody użytkownika.

Struktura repozytorium

AI-KNOWLEDGE-BASE/
├── AGENTS.md
├── README.md
├── docs.json
├── getting-started.md
├── guides/
├── knowledge/
├── projects/
│   ├── ai-agents/
│   ├── comfyui/
│   ├── gpu-backend/
│   └── lora-training-studio/
├── reference/
├── standards/
└── templates/

Dokumentacja online

Witryna dokumentacji:
https://lucas-sawicki-ai-knowledge-base-2.docs7.io/projects

Repozytorium GitHub:
https://github.com/Lucas-Sawicki/AI-KNOWLEDGE-BASE

Zasada nadrzędna

Repozytorium jest centralnym źródłem wiedzy projektowej. Każdy agent i każdy projekt powinien korzystać z istniejącej dokumentacji, aktualizować ją w kontrolowany sposób i unikać tworzenia równoległych, niespójnych źródeł informacji.