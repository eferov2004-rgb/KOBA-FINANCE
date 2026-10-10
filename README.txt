KOBA FINANCE — вход, регистрация и облачные данные
==================================================

Перед запуском требуется настроить Supabase. Без этого вход намеренно не работает.

1) Откройте https://supabase.com/ и создайте проект.
2) В проекте откройте SQL Editor → New query. Вставьте весь файл supabase_schema.sql и нажмите Run.
3) Откройте Project Settings → API (или Connect). Скопируйте Project URL и публичный anon/publishable key.
   Не используйте service_role/secret key.
4) В файле config.js замените YOUR_SUPABASE_PROJECT_URL и YOUR_SUPABASE_ANON_OR_PUBLISHABLE_KEY своими значениями.
5) Загрузите ВСЕ файлы архива в корень репозитория GitHub (сначала распакуйте архив).
6) GitHub → репозиторий → Settings → Pages → Deploy from a branch → main → /(root) → Save.
7) В Supabase → Authentication → URL Configuration добавьте URL опубликованного сайта в Site URL и Redirect URLs, например:
   https://ВАШ-ЛОГИН.github.io/KOBA-FINANCE/
8) Откройте сайт, зарегистрируйтесь, при необходимости подтвердите email из письма.

Возможности: вход, регистрация, восстановление пароля, финансовая сводка, доходы/расходы/закупки/продажи,
история операций, должники и отметка оплаты, отчёты, CSV и JSON backup/restore.

Безопасность: данные разделяются по аккаунтам через Row Level Security. Не делитесь паролем,
ключами или ссылкой восстановления. Импорт JSON добавляет записи, не заменяет существующие.
Сайт использует Supabase JS через CDN, поэтому для входа и работы с облаком нужен интернет.
