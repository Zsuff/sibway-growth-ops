# Sibway — 3 джерела правди

Складено 22.09.2026 як вхідний брифінг для Claude Cowork. Усі шляхи й посилання
нижче перевірені напряму (`find`, `git remote/branch/status`, `gh repo list`,
`gh issue list`, Google Docs/Sheets API) на момент складання — не з пам'яті чи
чужих переказів.

---

## Джерело 1: Локальні репозиторії (цей Mac)

### `sibway-website-` — код сайту (production runtime)
- **Шлях:** `/Users/zsuff/Documents/GitHub/sibway-website-`
- **GitHub remote:** `https://github.com/Zsuff/sibway-website-.git`
- **Призначення:** лише runtime-код статичного сайту (HTML/CSS/JS, `/uk/`, `/en/`, `/pl/`). За власним `DEPLOYMENT.md` цього репозиторію — **не** містить вимог, бізнес-документації чи деплой-доступів; нормативні правила веде `sibway-logistics-website`.
- **Стан:** гілка `main`, чисто, синхронізовано з `origin/main` (останній комміт `989f37c` — чернетки `content-drafts/import-poland.md` і `import-germany.md`).

### `sibway-logistics-website` — документація й вимоги проєкту
- **Шлях:** `/Users/zsuff/Documents/GitHub/sibway-logistics-website`
- **GitHub remote:** `https://github.com/Zsuff/sibway-logistics-website.git`
- **Призначення:** офіційне "джерело правди" для вимог — бренд, затверджений контент (`content/ua`, `content/en`, `content/pl`), макети (`design/approved`), правила й рішення (`docs/`), технічні чеклісти (`technical/`). Власний README прямо каже: код редагується тільки в `sibway-website-`, все інше — тут.
- **Стан:** гілка `main`, чисто, синхронізовано з `origin/main` (останній комміт `cc3f016`).

### `sibway-growth-ops` — маркетинг-опс (GTM/SEO Issues, правила контенту)
- **Локального клону на цьому Mac немає.** Усі зміни в цьому сесійному циклі велися напряму через `gh api`/`gh issue` без `git clone`.
- **GitHub remote:** `https://github.com/Zsuff/sibway-growth-ops.git`
- **Призначення:** `release-log.md`, `docs/seo/content-writing-rules.md`, `docs/seo/long-tail-keywords-and-customs-structure.md`, GitHub Issues для SEO-ТЗ.
- ⚠️ Цей репозиторій **ніде не згаданий** у README/RULES.md `sibway-logistics-website` — тобто формально він поза задокументованою схемою "джерел правди" цього проєкту (див. розділ "Відкриті розбіжності" нижче).

### ⚠️ Знайдено, але НЕ частина активного проєкту
- **Шлях:** `/Users/zsuff/Desktop/sibway-website`
- Це git-репозиторій **без жодного remote і без жодного комміту** (усе в staged/unstaged стані, "No commits yet"). Структура застаріла (плаский `src/`, шрифти Gilroy/TTNorms) — не відповідає актуальній `/uk/`, `/en/`, `/pl/` структурі. Схоже на покинутий ранній прототип. **Не використовувати як джерело для Cowork.**
- Інші знайдені директорії (`~/websites/sibway`, `~/Desktop/sibway-logistics-website`, `~/Downloads/...sibway.com.ua`, `~/Desktop/14-09-2026/www/sibway.com.ua`, кеші Webflow у Chrome IndexedDB) — **не git-репозиторії**, пропущено як нерелевантні.

---

## Джерело 2: GitHub

**Репозиторії:**
- Код сайту: https://github.com/Zsuff/sibway-website-
- Документація/вимоги: https://github.com/Zsuff/sibway-logistics-website
- Маркетинг-опс: https://github.com/Zsuff/sibway-growth-ops

**Відкриті/закриті Issues (`sibway-growth-ops`):**
- [#1](https://github.com/Zsuff/sibway-growth-ops/issues/1) — CLOSED — [GTM] Впровадити Google Tag Manager як центральний шар аналітики
- [#2](https://github.com/Zsuff/sibway-growth-ops/issues/2) — OPEN — [SEO-ТЗ] SEO-PAGE-001 — Import FTL Польща → Україна
- [#3](https://github.com/Zsuff/sibway-growth-ops/issues/3) — OPEN — [SEO-ТЗ] SEO-PAGE-002 — Import FTL Німеччина → Україна

**Ключові файли:**
- `content-writing-rules.md`: https://github.com/Zsuff/sibway-growth-ops/blob/main/docs/seo/content-writing-rules.md
- `long-tail-keywords-and-customs-structure.md`: https://github.com/Zsuff/sibway-growth-ops/blob/main/docs/seo/long-tail-keywords-and-customs-structure.md
- `content-drafts/` (готові чернетки посадкових сторінок): https://github.com/Zsuff/sibway-website-/tree/main/content-drafts
- `DEPLOYMENT.md` — ⚠️ існує **три** файли з такою назвою, не один (див. розбіжності нижче):
  - https://github.com/Zsuff/sibway-website-/blob/main/DEPLOYMENT.md
  - https://github.com/Zsuff/sibway-logistics-website/blob/main/docs/DEPLOYMENT.md
  - https://github.com/Zsuff/sibway-logistics-website/blob/main/technical/DEPLOYMENT.md

---

## Джерело 3: Google Drive

- **Головна папка "Sibway Logistics — Growth & Marketing":** https://drive.google.com/drive/folders/1_zFAu9GGXxE2ObZ5VYHdmZi8IXCulrH3
- **Marketing Operating System (Google Sheet):** https://docs.google.com/spreadsheets/d/17jBSYinc7I1VfY-YdxCGth7idCtEPn3QFcjzcm3dPf0/edit
- **Market Research: Ukraine–Europe Logistics (Google Doc):** https://docs.google.com/document/d/1ySND55V6sX_HBFafzvRVD3YAutE7n2239LDrEYXm_2M/edit
- **Target Segments, Client Personas & USP Hypotheses (Google Doc):** https://docs.google.com/document/d/1NuAhvQCS6KTELR4sTye2H_dLNRzEkDTVJ7QkTWQaNGM/edit
- **Конкурентна розвідка Maersk:** свідомо не включено (рішення власника, 22.09.2026) — Google Drive API вимкнена для GCP-проєкту `strong-augury-509119-t6`, автоматичний пошук був неможливий, а документ раніше ніде не згадувався.

---

## ⚠️ Відкриті розбіжності (виявлено під час звірки, не вирішено)

1. **Три файли `DEPLOYMENT.md`** — по одному в `sibway-website-` (каже "правила деінде") і два різних усередині `sibway-logistics-website` (`docs/DEPLOYMENT.md` і `technical/DEPLOYMENT.md`) з різним змістом. Який із двох в `sibway-logistics-website` є чинним — не встановлено.
2. **`sibway-growth-ops` не задокументований** у схемі "джерел правди" `sibway-logistics-website/README.md` і `docs/RULES.md` — формально третього репозиторію там не існує, хоча фактично в ньому вже є закритий Issue, 2 відкриті SEO-ТЗ і правила контенту.
3. **`docs/RULES.md` у `sibway-logistics-website` прямо забороняє push у `main` і merge без підтвердження власника** ("Одна задача — одна гілка — один pull request... Не виконувати push у main... без підтвердження власника"). У цій сесії пряме комічення в `main` `sibway-website-` і `sibway-growth-ops` відбувалося за явною командою власника щоразу окремо — формально узгоджено, але суперечить задокументованому правилу. Варто звірити, чи RULES.md досі чинний, чи потребує оновлення.
4. **На продакшн-домені `sibway.com.ua` досі стара версія сайту** (за словами `sibway-logistics-website/README.md`) — нова версія з `sibway-website-` ще не мігрована.

---

## Як користуватись Cowork із цим файлом

1. При старті сесії Cowork вкажи локальну робочу папку — **`/Users/zsuff/Documents/GitHub/sibway-website-`** для роботи з кодом сайту, або **`/Users/zsuff/Documents/GitHub/sibway-logistics-website`** для роботи з вимогами/контентом/документацією (залежно від задачі). `sibway-growth-ops` локального клону не має — для роботи з ним потрібен або `git clone https://github.com/Zsuff/sibway-growth-ops.git`, або виключно `gh api`/`gh issue` команди без клону.
2. Першим повідомленням сесії дай посилання на цей файл (`PROJECT_SOURCES_OF_TRUTH.md` у корені `sibway-growth-ops`), щоб Cowork одразу мав повну карту репозиторіїв, Issues і Drive-документів без повторного пошуку.
3. Перед будь-якими змінами Cowork має прочитати `docs/RULES.md` і `docs/CLAUDE.md` у `sibway-logistics-website` — там задокументовані обов'язкові правила роботи (одна задача — одна гілка — один PR, заборона push у main без підтвердження, заборона вигадувати факти).
4. Розбіжності з розділу вище варто показати власнику при першій нагоді, а не тихо ігнорувати — вони впливають на те, який файл/репозиторій вважати чинним.
