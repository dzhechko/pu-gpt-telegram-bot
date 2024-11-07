# GPT Telegram Bot

## 📝 Описание
Многофункциональный Telegram бот, работающий с текстом и изображениями через OpenAI API. Поддерживает как генерацию текста с помощью GPT моделей, так и создание/редактирование изображений.

## 🚀 Основные возможности
- Генерация текста с использованием различных GPT моделей
- Создание изображений по текстовому описанию
- Создание вариаций существующих изображений
- Настраиваемые параметры для текстовых и графических моделей
- История сообщений с возможностью очистки
- Поддержка групповых чатов
- Потоковый режим ответов (streaming)

## ⚙️ Настройки текстовой модели
- Базовый URL API
- Выбор модели (GPT-3.5-turbo, GPT-4, GPT-4-turbo, GPT-4o-mini или пользовательская)
- Температура генерации (0-1)
- Максимальное количество токенов
- Опциональное использование внешнего AI-ассистента

## 🎨 Настройки генерации изображений
- Базовый URL API
- Выбор модели (DALL-E 3, DALL-E 2, Stable Diffusion XL, Midjourney API)
- Размер изображения
- Качество (стандартное/HD)
- Стиль (натуральный/яркий/аниме)
- HDR режим

## 🛠 Технические требования
- Python 3.11+
- python-telegram-bot[job-queue]==20.8
- openai==1.12.0
- SQLAlchemy==2.0.27
- Остальные зависимости в requirements.txt

## 📦 Установка и запуск

1. Клонируйте репозиторий:
```bash
git clone [URL репозитория]
cd [название директории]
```

2. Установите зависимости:
```bash
pip install -r requirements.txt
```

3. Создайте файл .env со следующими переменными:
```env
TELEGRAM_TOKEN=ваш_токен_бота
OPENAI_API_KEY=ваш_ключ_api_openai
DEBUG_MODE=False  # True для режима отладки
```

4. Запустите бота:
```bash
python bot.py
```

## 🤖 Использование бота

### Основные команды:
- `/start` - Начало работы с ботом
- `/help` - Справка по командам
- `/settings` - Настройки текстовой модели
- `/image_settings` - Настройки генерации изображений
- `/history` - История сообщений
- `/clear_history` - Очистить историю

### Работа с текстом:
- Просто отправьте сообщение боту для генерации текста
- Настройте параметры модели через меню /settings

### Работа с изображениями:
- `/image [описание]` - Создать изображение по описанию
- Отправьте изображение для создания его вариации
- Настройте параметры через меню /image_settings

## 🔧 Отладка
- Установите DEBUG_MODE=True в .env для подробного логирования
- Логи сохраняются в директории logs/ (в режиме отладки) или в системной временной директории
- Используйте команду /debug в режиме отладки для получения технической информации

## 🚂 Деплой на Railway.app
1. Создайте новый проект на Railway
2. Подключите репозиторий
3. Добавьте переменные окружения (TELEGRAM_TOKEN, OPENAI_API_KEY)
4. Railway автоматически определит Procfile и выполнит деплой

## 📄 Лицензия
[MIT License](https://opensource.org/licenses/MIT)

Проект распространяется под лицензией MIT. Подробнее о лицензии можно узнать по [ссылке](https://opensource.org/licenses/MIT).

## 👥 Автор
Дмитрий Жечков ([GitHub](https://github.com/dzhechko))