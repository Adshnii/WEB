# Сайт SOLVIX — паспорт проекта

**Живой сайт: https://solvixcompany.com**

Этот файл — справка по всем настройкам сайта: что где находится, какие
правила подключены и как проверить, что всё работает. Обновляется при
каждом значимом изменении.

---

## 1. Из чего состоит система

| Часть | Где | Детали |
|---|---|---|
| Домен | Namecheap, аккаунт `adshnii` | solvixcompany.com, куплен 24.07.2026, оплачен до **24.07.2027**, автопродление ВКЛ, Domain Privacy ВКЛ |
| Файлы сайта | Этот репозиторий (Adshnii/WEB), ветка `main` | GitHub Pages публикует их автоматически при каждом push |
| Хостинг | GitHub Pages | Бесплатно, без ежемесячных платежей |
| Локальная копия | `/Users/a.dshnii/WEB` на Маке | Синхронизирована с репозиторием через git |
| Почта | Namecheap Email Forwarding | info@solvixcompany.com → tolik.dolishniy@gmail.com (пересылка, не отдельный ящик) |

⚠️ **solvix-company.com (с дефисом) — ЧУЖОЙ домен.** Никогда не указывать
его в документах, на визитках и в переписке. Наш домен — без дефиса.

## 2. Файлы сайта

| Файл | Что это |
|---|---|
| `index.html` | Весь сайт одной страницей (фото зашиты внутрь файла) |
| `privacy.html` | Privacy Policy — обязательна: на сайте есть форма и возможна аналитика |
| `terms.html` | Terms of Service — правила пользования сайтом, оговорка что цены = предварительная оценка |
| `accessibility.html` | ADA/Accessibility statement — рекомендована для бизнеса во Флориде, снижает риск исков |
| `CNAME` | Привязка домена к GitHub Pages — **не удалять и не редактировать** |
| `sitemap.xml` | Карта сайта для Google |
| `robots.txt` | Разрешение поисковикам индексировать сайт |
| `README.md` | Этот файл |

## 3. DNS-записи (Namecheap → Advanced DNS)

Если сайт вдруг перестанет открываться — сверить записи с этой таблицей:

| Тип | Host | Значение | Зачем |
|---|---|---|---|
| A | @ | 185.199.108.153 | GitHub Pages |
| A | @ | 185.199.109.153 | GitHub Pages |
| A | @ | 185.199.110.153 | GitHub Pages |
| A | @ | 185.199.111.153 | GitHub Pages |
| CNAME | www | adshnii.github.io | www-версия → основной сайт |
| MX (Mail Settings = Email Forwarding) | @ | eforward*.registrar-servers.com | Пересылка почты info@ |

Настройки почты и DNS живут в Namecheap: Domain List → solvixcompany.com →
Manage → Advanced DNS (записи) и вкладка Domain → Redirect Email (пересылка).

## 4. HTTPS / сертификат

- Сертификат выпущен GitHub автоматически 24.07.2026 (Let's Encrypt).
- «Enforce HTTPS» включён: любой заход по http:// сам перенаправляется на https://.
- Продлевается автоматически, делать ничего не нужно.

## 5. Форма заявок (Get a Quote)

- Работает через сервис **FormSubmit (formsubmit.co)** — бесплатно, без сервера.
- Заявки приходят на info@solvixcompany.com → падают в Gmail.
- ❗ **Одноразовая активация:** после первой отправки формы FormSubmit
  присылает письмо «Confirm» на почту — надо нажать подтверждение,
  иначе заявки не доставляются. Статус: ожидает активации.

## 6. SEO — что подключено

- **Schema.org LocalBusiness (GeneralContractor)** в `index.html`: название
  Solvix Company Naples, телефон +1-239-776-0639, адрес 132 Bedzel Cir
  Naples FL 34104, зона Naples/Fort Myers/Miami, часы работы — данные
  совпадают с Google Business Profile (это важно для локальной выдачи).
- Canonical, Open Graph теги, title + meta description.
- `sitemap.xml` + `robots.txt`.
- Правовые страницы помечены noindex (в поиске нужна главная, а не они).

## 7. Как проверить, что всё работает

1. **Сайт жив:** открыть https://solvixcompany.com — замочек, страница грузится.
2. **www работает:** https://www.solvixcompany.com — перенаправляет на основной.
3. **Почта:** отправить письмо на info@solvixcompany.com с любого ящика —
   через минуту оно в Gmail (tolik.dolishniy@gmail.com).
4. **Правовые страницы:** ссылки Privacy / Terms / Accessibility внизу сайта.
5. **Разметка для Google:** https://search.google.com/test/rich-results →
   ввести solvixcompany.com → должен увидеть LocalBusiness.
6. **Хостинг-статус:** в этом репозитории → Settings → Pages → зелёная
   галочка у solvixcompany.com.

## 8. Что ещё не сделано (план)

- [ ] Активировать форму (нажать Confirm в письме от FormSubmit) — **вручную**
- [ ] Google Search Console: подтвердить домен, отправить sitemap
- [ ] Google Analytics 4 (опционально)
- [ ] Google Business Profile: поле Website сменить с Facebook на сайт
- [ ] Добавить сайт в профиль Facebook
- [ ] Отправка писем «от имени» info@ (нужен Private Email ~$15/год или Zoho) — если понадобится

## 9. История изменений

| Дата | Что сделано |
|---|---|
| 24.07.2026 | Домен куплен; DNS настроен; сайт опубликован; HTTPS включён; почта info@ настроена |
| 25.07.2026 | Правовые страницы (Privacy/Terms/Accessibility); LocalBusiness-разметка; sitemap; robots; этот README |
