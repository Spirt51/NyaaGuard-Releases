<p align="center">
  <img src="assets/nyaaguard-logo.png" width="560" alt="NyaaGuard">
</p>

<p align="center">
  <a href="README.md"><strong>Русский</strong></a> ·
  <a href="docs/README.uk.md">Українська</a> ·
  <a href="docs/README.en.md">English</a> ·
  <a href="docs/README.de.md">Deutsch</a>
</p>

<p align="center">
  <a href="https://github.com/Spirt51/NyaaGuard-Releases/releases/latest"><img src="https://img.shields.io/github/v/release/Spirt51/NyaaGuard-Releases?display_name=tag&style=for-the-badge&color=b91c1c" alt="Последний релиз"></a>
  <img src="https://img.shields.io/badge/Windows-x64-2563eb?style=for-the-badge&logo=windows11&logoColor=white" alt="Windows x64">
  <img src="https://img.shields.io/badge/Linux-amd64-f59e0b?style=for-the-badge&logo=linux&logoColor=white" alt="Linux amd64">
</p>

<h1 align="center">NyaaGuard</h1>

<p align="center">
  Защита переходов по ссылкам для Windows и Linux.<br>
  Очистка URL, локальные базы угроз, анализ перенаправлений и дополнительная проверка через VirusTotal.
</p>

> [!IMPORTANT]
> Это публичный репозиторий официальных сборок и метаданных обновления. Исходный код NyaaGuard хранится в приватном репозитории.

## Что умеет NyaaGuard

- перехватывает внешние ссылки и передаёт безопасные переходы в выбранный браузер;
- удаляет распространённые параметры отслеживания из URL: `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`, `utm_term`, `fbclid`, `gclid`, `dclid`, `msclkid` и другие рекламные/аналитические идентификаторы;
- проверяет домены и точные URL по обновляемым базам фишинга, вредоносных и спам-ресурсов;
- поддерживает отдельный отключаемый фильтр adult/NSFW;
- проверяет цепочку перенаправлений и коды ответа веб-серверов;
- при наличии пользовательского API-ключа выполняет дополнительную проверку неизвестных ссылок через VirusTotal;
- поддерживает пользовательские списки блокировки и исключений, прокси, системную тему и четыре языка;
- работает в фоне и сворачивается в системный трей.

NyaaGuard сохраняет функциональные параметры — например идентификатор страницы, товара, сообщения или видео — чтобы очищенная ссылка продолжала работать. После очистки проверяется итоговый URL и вся обнаруженная цепочка перенаправлений.

## Защита файлов в 0.2.0

- новый антивирусный центр с быстрой, выборочной и полной проверкой;
- проверка отдельных файлов, папок, нескольких дисков или всего компьютера;
- SHA-256, определение реального формата, статический анализ и выявление подмены расширения;
- изолированный YARA-X с правилами ReversingLabs и отобранными Signature-Base;
- необязательная проверка хэшей через MalwareBazaar, URLhaus и VirusTotal с пользовательскими API-ключами;
- SQLite-кэш и журнал, пауза/возобновление, мониторинг папок загрузок и съёмных дисков;
- зашифрованный карантин с проверкой SHA-256 при восстановлении;
- безопасная реакция на угрозу: «В карантин», «Пропустить» или «В исключения»;
- действия с файлами требуют подтверждения по умолчанию;
- контекстное меню проверки файлов, папок и дисков в Windows и Linux.

Проверка работает и без API-ключей: локальные SHA-256, формат, эвристика и YARA-X остаются доступными. Содержимое файла не отправляется в сервисы репутации — используется только хэш.

## Скачать

Все официальные сборки находятся на странице **[последнего релиза](https://github.com/Spirt51/NyaaGuard-Releases/releases/latest)**.

| Система | Пакет | Назначение |
|---|---|---|
| Windows 10/11 x64 | `NyaaGuard-Setup-*-win-x64.exe` | Установка или портативная распаковка, служба и ярлыки — на выбор |
| Debian / Ubuntu amd64 | `nyaaguard_*_amd64.deb` | Установка приложения, Native Messaging и пользовательской службы systemd |

**Актуальная версия 0.2.0:**

- [Скачать NyaaGuard для Windows x64](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/NyaaGuard-Setup-0.2.0-win-x64.exe) · [SHA-256](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/NyaaGuard-Setup-0.2.0-win-x64.exe.sha256)
- [Скачать NyaaGuard для Debian/Ubuntu amd64](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/nyaaguard_0.2.0_amd64.deb) · [SHA-256](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/nyaaguard_0.2.0_amd64.deb.sha256)

### Проверка файла

Для каждого пакета опубликован файл `.sha256`.

```powershell
# Windows PowerShell
Get-FileHash .\NyaaGuard-Setup-0.2.0-win-x64.exe -Algorithm SHA256
```

```bash
# Linux
sha256sum -c nyaaguard_0.2.0_amd64.deb.sha256
sudo apt install ./nyaaguard_0.2.0_amd64.deb
```

> [!NOTE]
> Сборки пока не подписаны коммерческим сертификатом. Windows SmartScreen может показать предупреждение для нового приложения — перед запуском сверяйте SHA-256 с опубликованным файлом.

## Обновления

NyaaGuard автоматически проверяет наличие новой версии раз в час. Стабильный канал использует [`update-manifest.json`](update-manifest.json): приложение получает пакет по HTTPS и сверяет его SHA-256 до установки.

## Конфиденциальность

Основные проверки выполняются локально. URL отправляется в VirusTotal только если пользователь сам добавил API-ключ, ссылка отсутствует в локальных базах и онлайн-проверка включена. Ключ хранится локально отдельно от обновляемых файлов программы.

## Расширение Firefox

Расширение Firefox находится в разработке и пока не входит в опубликованные релизы.

## Поддержать проект

Если NyaaGuard оказался полезен, вы можете поддержать дальнейшую разработку:

| Сеть | Адрес |
|---|---|
| USDT — TRC20 | `TR3fkALFRTDyRaHsDU8aUmANGPRDy2gU1s` |
| ETH — ERC20 | `0x9d20248c779dcb742f7795a0c7461346c0c8934e` |
| BTC | `1BQwypiKfhNGb1ryKzdp7TBPL4wR6ckU4J` |
| PayPal | `spirt51@hotmail.com` |

> Перед переводом криптовалюты обязательно проверьте выбранную сеть и адрес.

## Журнал изменений и обратная связь

- **[Журнал изменений](CHANGELOG.md)**
- **[Сообщить об ошибке или предложить улучшение](https://github.com/Spirt51/NyaaGuard-Releases/issues)**
- **[Все релизы](https://github.com/Spirt51/NyaaGuard-Releases/releases)**

<p align="center"><sub>NyaaGuard — спокойнее открывайте ссылки, не отдавая трекерам лишнее.</sub></p>
