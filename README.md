# Token Calculator — Claude Pro

Веб-инструмент для контроля расхода токенов на плане Claude Pro ($20/мес).

## Локальное использование (Mac)

Двойной клик на `index.html` → открывается в браузере.

## Деплой на Vercel (доступ с iPhone когда Mac выключен)

1. Зайти на **vercel.com** → войти в аккаунт (или зарегистрироваться)
2. Нажать **Add New → Project**
3. Внизу найти **"Or deploy without a Git repository"** → выбрать **"Browse"**
4. Загрузить папку `token-calculator` (или только `index.html`)
5. Нажать **Deploy**
6. После деплоя получить URL вида `https://token-calculator-xxx.vercel.app`

**URL после деплоя:** https://claude-token-calculator.vercel.app

## Альтернатива: локальная сеть (Mac должен быть включён)

```bash
cd ~/Documents/VS\ Claude\ Code/token-calculator
python3 -m http.server 8080
```

Затем на iPhone открыть: `http://[IP-адрес-Mac]:8080`

IP-адрес Mac: Системные настройки → Wi-Fi → Подробнее → IP-адрес

## Обновление DEFAULT_OVERHEAD

1. В Claude Code запустить `/cost` (показывает токены текущей сессии)
2. Открыть калькулятор → изменить поле **Overhead** на полученное число
3. Значение сохранится в localStorage автоматически

## Лимиты Claude Pro

| Окно | Лимит |
|------|-------|
| 5 часов | 44 000 токенов |
| 7 дней | ~300 000 токенов (оценка) |

## Обновление файла

Открыть `index.html` в любом редакторе и сохранить.
После изменений — повторно загрузить на Vercel (drag & drop).
