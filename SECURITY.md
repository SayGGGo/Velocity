# Безопасность

[← Обзор проекта](https://github.com/SayGGGo/Velocity/blob/main/)

<a href="https://isvelocity.ru/"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/SayGGGo/VelocityReadmeAssets/main/security-dark-789bbb6d7ebf.png"><source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/SayGGGo/VelocityReadmeAssets/main/security-light-c7344d674489.png"><img src="https://raw.githubusercontent.com/SayGGGo/VelocityReadmeAssets/main/security-dark-789bbb6d7ebf.png" width="980" alt="security — Velocity" /></picture></a>

Область сопровождения: текущая основная ветка фронтенда и связанный backend
бэкенда. Старые снимки не имеют отдельной гарантии обновлений.

Сообщайте об уязвимостях приватно: через GitHub Private Vulnerability Reporting,
если он включён, либо тикет на [isvelocity.ru](https://isvelocity.ru/) для SayGGGo.
При недоступности сайта используйте доступный приватный канал сопровождающего.
Не создавайте публичное issue с эксплойтом, токенами или персональными данными.

Укажите компонент, шаги воспроизведения, ожидаемый и фактический результат,
влияние, версию и минимальный безопасный пример. Удалите секреты из приложений.
Не атакуйте чужие аккаунты, не извлекайте реальные данные и не создавайте нагрузку.
Наличие этого документа не является разрешением на тестирование продакшена.
Срок ответа и вознаграждение не гарантируются; disclosure согласуется с автором.

В исходниках реализованы:

- Secure / HttpOnly / SameSite=Lax cookies; CSRF-проверки изменяющих запросов.
- Хеширование паролей Werkzeug; ограничения запросов и проверки сессии на сервере.
- Проверка подписи уведомлений RoboKassa, сверка счёта и защита от повторного зачисления.
- Заголовки nosniff, DENY и ограниченная передача Referer во frontend `_headers`.
- OIDC для публикации README: проверка репозитория, ветки, workflow и повторов токена.

Это описание кода, не независимый аудит и не гарантия развёртывания всех настроек.
Обфускация имён CSS не является защитой доступа. Браузерный код доступен пользователю.
Ключи провайдеров и платёжные секреты должны оставаться на сервере, вне Git.

<p align="center">
<a href="https://isvelocity.ru/"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/SayGGGo/VelocityReadmeAssets/main/safety-dark-8464af649500.png"><source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/SayGGGo/VelocityReadmeAssets/main/safety-light-1ca71ab32794.png"><img src="https://raw.githubusercontent.com/SayGGGo/VelocityReadmeAssets/main/safety-dark-8464af649500.png" width="980" alt="Защита: GG Protect, HTTPS API, серверная проверка доступа и платежей. Публичные показатели обезличены." /></picture></a>
</p>
