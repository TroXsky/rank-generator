# DragoriaStudio Rank Generator — GitHub Pages

To jest gotowa, **bezstanowa** wersja strony do publikacji na GitHub Pages.

- brak zapisywania paczek w przeglądarce,
- brak `localStorage`,
- brak panelu zarządzania paczkami,
- po odświeżeniu wracają domyślne rangi i domyślny język.

Wszystkie pliki są statyczne — nie potrzebujesz Node.js ani serwera na produkcji.

## Szybki deploy (ręcznie)

1. Utwórz nowe repozytorium na GitHubie.
2. Wgraj **zawartość tego folderu** do katalogu głównego repozytorium.
3. Wejdź w **Settings → Pages**.
4. Wybierz **Deploy from a branch**.
5. Ustaw branch **main** i katalog **/ (root)**.
6. Zapisz — GitHub opublikuje stronę pod adresem
   `https://<twoj-user>.github.io/<nazwa-repo>/`.

## Deploy przez GitHub Actions

Jeśli wgrywasz cały projekt (nie tylko ten folder):

1. Wgraj repozytorium na GitHub.
2. **Settings → Pages → Source: GitHub Actions**.
3. Push na `main` uruchomi workflow, który zbuduje wersję bezstanową
   (`npm run build:github`) i opublikuje katalog `docs/`.

## Podgląd lokalny

```bash
npm run build:github
```

Następnie na Windows uruchom `start-github.bat` albo:

```bash
set SERVE_DIR=docs
set PORT=4174
node serve.cjs
```

Strona będzie dostępna pod <http://localhost:4174>.

## English

This is a ready-to-deploy, **stateless** GitHub Pages build:

- no pack saving in the browser,
- no `localStorage`,
- no pack manager,
- refreshing restores default ranks and the default language.

Upload the **contents** of this folder to a GitHub repository root, then open
**Settings → Pages**, choose **Deploy from a branch**, branch **main**, folder
**/ (root)**.

The full project also includes a GitHub Actions workflow that builds this
stateless version and deploys the `docs/` directory automatically.

Created by **TroXsky** · DragoriaStudio
