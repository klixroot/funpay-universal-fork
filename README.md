# FunPay Universal (Fork)

Современный модульный бот-помощник для торговой площадки **FunPay**.

> Это форк/стартер на основе оригинального репозитория [alleexxeeyy/funpay-universal](https://github.com/alleexxeeyy/funpay-universal).

## Основные возможности

- Автовыдача товаров сразу после оплаты
- Автоответчик в чатах
- Автоподнятие лотов
- Поддержка прокси (HTTP/SOCKS5)
- **Модульная система** — легко добавлять свои плагины
- Гибкая конфигурация (INI)

## Установка

### Требования
- Python **3.12+**
- Git

### Windows
```bash
git clone https://github.com/klixroot/funpay-universal-fork.git
cd funpay-universal-fork
# Запусти install.bat или создай виртуальное окружение
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

### Linux / macOS
```bash
git clone https://github.com/klixroot/funpay-universal-fork.git
cd funpay-universal-fork
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Запуск

```bash
python main.py
# или через start.bat / launcher
```

## Разработка модулей

Плагины находятся в папке `plugins/`.

Пример структуры плагина:
```python
# plugins/my_module.py
class MyModule:
    def __init__(self, bot):
        self.bot = bot
    
    def on_order_paid(self, order):
        # логика автовыдачи
        pass
```

## Полезные ссылки
- Оригинал: https://github.com/alleexxeeyy/funpay-universal
- Телеграм-бот автора для модулей: @alexey_production_bot
- Канал: t.me/alexeyproduction

## Git команды (основные)

| Команда | Описание |
|--------|-------------|
| `git clone <url>` | Клонировать репо |
| `git status` | Посмотреть изменения |
| `git add .` | Добавить все изменения |
| `git commit -m "текст"` | Закоммитить |
| `git push` | Отправить на GitHub |
| `git pull` | Получить обновления |
| `git branch -M main` | Переименовать ветку |
| `git checkout -b feature/new-module` | Создать новую ветку |

**Рекомендуется работать в отдельной ветке** и делать Pull Request в `main`.

---

Создано с помощью Grok. Приятной работы!