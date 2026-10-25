# Octane 3D Positional Voice Server (LiveKit Cloud Edition)

Полноценный 3D позиционный голосовой чат для Roblox Octane (2021) на базе **LiveKit Cloud SFU** и **Web Audio API**.

## Особенности LiveKit Cloud:
- **SFU Медиа-сервера**: отсутствие проблем со сложными NAT, мобильным интернетом или закрытыми портами.
- **3D звук (HRTF Panning)**: чистейший Opus-звук в наушниках с точным расчетом угла и дистанции до персонажа в игре.
- **Вход по 4-значному коду**: команда `/voice` в Roblox выдает 4-значный пин-код, игрок вводит его на сайте без логинов и скачиваний.
- **Roblox оверхед-бабл**: классическое облачко диалога с пульсирующими иконками громкости над головой говорящего.
- **HUD микрофона**: отображение статуса микрофона и громкости в игре.

## Переменные окружения (Environment Variables):
Уже вшиты в `server.js`, но при желании можно задать в настройках Render / Railway:
- `LIVEKIT_URL`: `wss://octanevc-tzsmlvtk.livekit.cloud`
- `LIVEKIT_API_KEY`: `APIjydps4NRHmtk`
- `LIVEKIT_API_SECRET`: `siZGYI37k68aSd4nSqkjcr2d1kKzzgoRansVNcmJf8f`
- `PORT`: порт HTTP сервера (по умолчанию `3000`).

## Деплой на Render.com (Бесплатно, 1 клик):
1. Загрузите файлы этого проекта в свой GitHub репозиторий.
2. Откройте [render.com](https://render.com) и нажмите **New -> Web Service**.
3. Подключите ваш GitHub репозиторий.
4. Render автоматически выставит:
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
5. Нажмите **Deploy**.
6. Скопируйте полученный URL (например `https://my-voice.onrender.com`) и пропишите его в Roblox в модуле:
   `ReplicatedStorage.VoiceChat.VoiceConfig.SERVER_URL`.

## Локальный запуск (для проверки):
```bash
npm install
npm start
```
Сервер будет доступен по адресу `http://localhost:3000`.
