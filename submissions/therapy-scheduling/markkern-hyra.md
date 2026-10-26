# Здача WS7

## Дані

- Роль: dev
- Команда: therapy-scheduling
- GitHub-логін: markkern-hyra
- Ваше репо: https://github.com/markkern-hyra/therapy-scheduling
- SHA: 5704a52a4b79772c5e0b838910f2650dbc1072a3
- Репо вимог PM: https://github.com/Sofiia-pm/therapy-scheduling-spec
- Прод-URL: https://therapy-scheduling-theta.vercel.app

## PM

—

## Розробник

- Рядок «Вимоги:» з `docs/conformance.md` на SHA: Вимоги: https://github.com/Sofiia-pm/therapy-scheduling-spec · джерело: issues · знімок 2026-10-26
- PR «Оновлення вимог» зі зрізом 2 (A): https://github.com/markkern-hyra/therapy-scheduling/pull/9
- PR «Оновлення вимог» після уточнень PM (A): `/requirements-sync 2026-10-26: Вимоги актуальні` (issues https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/1, https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/2, https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/19 не змінювались після знімка 2026-10-26 з https://github.com/markkern-hyra/therapy-scheduling/pull/9)
- Питання в репо PM (A; щонайменше 2, з них щонайменше 1 — власне issue): https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/27, https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/28, https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/29
- PR «Специфікація» з `add-<зріз2>` (A): https://github.com/markkern-hyra/therapy-scheduling/pull/12
- Дизайн-система — PR (B): https://github.com/markkern-hyra/therapy-scheduling/pull/10 (розвиток DS і візуальний цикл — https://github.com/markkern-hyra/therapy-scheduling/pull/18; теплий напрям за аудитом дизайну — https://github.com/markkern-hyra/therapy-scheduling/pull/20)
- Дизайн-система — `DESIGN.md` і джерело (B): https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/DESIGN.md · джерело: артефакт Claude Design (Design System «Therapy Scheduling»)
- Дизайн-система — прогін `architecture` на `main` (B): https://github.com/markkern-hyra/therapy-scheduling/actions/runs/40356518801
- Знімки «до/після» (B): https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-before-login-light.png, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-after-login-light.png (усі — `docs/img/ws7-before-*`, `docs/img/ws7-after-*`)
- Зміна `impl-<зріз2>` (C): https://github.com/markkern-hyra/therapy-scheduling/tree/5704a52a4b79772c5e0b838910f2650dbc1072a3/openspec/changes/archive/2026-10-26-impl-client-cards
- PR-и задач «Реалізація» (C; щонайменше 2): https://github.com/markkern-hyra/therapy-scheduling/pull/16, https://github.com/markkern-hyra/therapy-scheduling/pull/17
- Мутаційна перевірка — червоні прогони (C; щонайменше 2): https://github.com/markkern-hyra/therapy-scheduling/actions/runs/40321541872 (AC-CARD-06), https://github.com/markkern-hyra/therapy-scheduling/actions/runs/40324533067 (AC-CARD-05)
- ADR (D): https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/decisions/0006-roles-in-profiles-no-admin-client.md, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/decisions/0007-therapist-own-clients-in-rls.md, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/decisions/0008-warm-design-direction.md
- Архітектурне правило, крім `check:design` (D): job «Секретний ключ лише на сервері» (`check:boundary`) у `.github/workflows/architecture.yml`; червоний прогін на коміті з навмисним порушенням: https://github.com/markkern-hyra/therapy-scheduling/actions/runs/40328131750 (job «Секретний ключ лише на сервері» — failure на тимчасовій сторінці "use client", що читає SUPABASE_SECRET_KEY; revert у тому самому PR https://github.com/markkern-hyra/therapy-scheduling/pull/18; ADR 0006 посилається на правило)
- Акаунти для PM (E): admin1@example.test (admin), scheduler1@example.test (scheduler), therapist1@example.test (therapist), newuser1@example.test (без ролі); адреси — у `supabase/demo-users.json`, архів з акаунтами — `accounts.zip` (AES-256) у корені репо. Паролі — PM у чаті, не тут
- Скріни за ролями (E): https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-role-scheduler-clients.png, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-role-scheduler-new-error.png, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-role-therapist-clients.png, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-role-therapist-denied.png, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-role-therapist-new-denied.png, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-role-admin-clients.png, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-role-norole.png, https://github.com/markkern-hyra/therapy-scheduling/blob/5704a52a4b79772c5e0b838910f2650dbc1072a3/docs/img/ws7-role-signed-out-clients.png (опис — https://github.com/markkern-hyra/therapy-scheduling/pull/19)
- AC зрізу 2 (E): AC-CARD-01 (реалізовано), AC-CARD-02 (реалізовано), AC-CARD-03 (реалізовано), AC-CARD-04 (реалізовано), AC-CARD-05 (реалізовано), AC-CARD-06 (реалізовано), AC-CARD-07 (реалізовано), AC-CARD-08 (реалізовано), AC-CARD-09 (реалізовано), AC-CARD-10 (реалізовано), AC-CARD-11 (реалізовано)
- Відхилення від PM (E): не надходило

## Бонус

Цикл візуальної перевірки в браузері агента — https://github.com/markkern-hyra/therapy-scheduling/pull/18 і https://github.com/markkern-hyra/therapy-scheduling/pull/20.

Як: агент піднімав локальний Supabase у Docker з усіма міграціями й синтетичними даними AC, запускав застосунок і Playwright у Chrome. Знімав кожну сторінку × роль × світлу й темну тему × 390px, по кілька проходів у кожному PR.

- **#18.** Знайшов і виправив різну висоту полів і кнопок, шапку без поточного розділу, порожню головну, головну дію у вигляді посилання, форму з полями дорослого й дитини водночас, поламану шапку на 390px.
- **#20.** Людина оцінила вигляд як «так собі». Агент зробив аудит дизайну: 16 знахідок P1–P3, тепла палітра з розрахунком контрасту, три шрифти, макети компонентів; рішення погоджено питаннями до людини. Потім переробив дизайн-систему: теплі нейтральні, Figtree з табличними цифрами, іконки lucide з підписом, розклад списком по днях, пісочний «Held». Під час перезйомки знайшов і виправив ще дві вади: розтягнуту кнопку фільтра і розірване «Held until» на 390px.
- **Свідомо пропустив** формат нативного поля дати — його задає браузер.

Що з цього випливає: рішення про вигляд тепер зафіксовані в DESIGN.md і ADR 0008, тож наступні екрани агент збирає з тих самих частин і перевіряє тим самим циклом.
