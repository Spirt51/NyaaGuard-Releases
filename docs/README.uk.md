<p align="center"><img src="../assets/nyaaguard-logo.png" width="560" alt="NyaaGuard"></p>

<p align="center">
  <a href="../README.md">Русский</a> ·
  <a href="README.uk.md"><strong>Українська</strong></a> ·
  <a href="README.en.md">English</a> ·
  <a href="README.de.md">Deutsch</a>
</p>

<p align="center">
  <a href="https://github.com/Spirt51/NyaaGuard-Releases/releases/latest"><img src="https://img.shields.io/github/v/release/Spirt51/NyaaGuard-Releases?display_name=tag&style=for-the-badge&color=b91c1c" alt="Останній випуск"></a>
  <img src="https://img.shields.io/badge/Windows-x64-2563eb?style=for-the-badge&logo=windows11&logoColor=white" alt="Windows x64">
  <img src="https://img.shields.io/badge/Linux-amd64-f59e0b?style=for-the-badge&logo=linux&logoColor=white" alt="Linux amd64">
</p>

<h1 align="center">NyaaGuard</h1>
<p align="center">Захист переходів за посиланнями для Windows і Linux.<br>Очищення URL, локальні бази загроз, аналіз перенаправлень і додаткова перевірка через VirusTotal.</p>

> [!IMPORTANT]
> Це публічний репозиторій офіційних збірок і метаданих оновлення. Вихідний код NyaaGuard зберігається у приватному репозиторії.

## Можливості

- перехоплення зовнішніх посилань і відкриття безпечних адрес у вибраному браузері;
- видалення поширених параметрів відстеження: `utm_*`, `fbclid`, `gclid`, `dclid`, `msclkid` та інших рекламних/аналітичних ідентифікаторів;
- локальні оновлювані бази фішингу, шкідливих і спам-ресурсів;
- окремий вимиканий фільтр adult/NSFW;
- перевірка ланцюжка перенаправлень і кодів відповіді;
- додаткова перевірка невідомих URL через VirusTotal із власним API-ключем;
- користувацькі списки блокування та винятків, проксі, системна тема, чотири мови й робота в треї.

Функціональні параметри сторінки, товару, повідомлення чи відео зберігаються. Після очищення NyaaGuard перевіряє підсумковий URL і весь виявлений ланцюжок перенаправлень.

## Захист файлів у 0.3.0

- новий антивірусний центр зі швидкою, вибірковою та повною перевіркою;
- перевірка окремих файлів, папок, кількох дисків або всього комп’ютера;
- SHA-256, визначення реального формату, статичний аналіз і виявлення підміни розширення;
- ізольований YARA-X із правилами ReversingLabs та відібраними Signature-Base;
- необов’язкова перевірка хешів через MalwareBazaar, URLhaus і VirusTotal із користувацькими API-ключами;
- SQLite-кеш і журнал, пауза/продовження, моніторинг завантажень і знімних дисків;
- зашифрований карантин із перевіркою SHA-256 під час відновлення;
- безпечний вибір дії: карантин, пропустити або додати SHA-256 до винятків;
- дії з файлами за замовчуванням потребують підтвердження;
- контекстне меню перевірки файлів, папок і дисків у Windows та Linux.

Перевірка працює без API-ключів: локальні хеші, формат, евристика та YARA-X залишаються доступними. Вміст файлу не надсилається сервісам репутації — використовується лише хеш.

У 0.3.0 файловий конвеєр і кеш суттєво прискорено. В A/B-тесті на 20 000 операцій відсутні записи кешу оброблялися до **40,8 раза швидше**, повторні звернення — до **50,8 раза швидше**, пакетний запис журналу — до **49,5 раза швидше** за попередню реалізацію. Це показники окремих операцій кешу й журналу; швидкість повної перевірки залежить від накопичувача, набору файлів і ввімкнених рушіїв.

У версії 0.3.0 оновлення програми виконується в тихому режимі з автоматичним відновленням фонової служби. Ключі VirusTotal і abuse.ch зберігаються окремо від файлів програми та не втрачаються під час оновлення.

## Завантаження

Офіційні пакети доступні в **[останньому випуску](https://github.com/Spirt51/NyaaGuard-Releases/releases/latest)**.

| Система | Пакет | Призначення |
|---|---|---|
| Windows 10/11 x64 | `NyaaGuard-Setup-*-win-x64.exe` | Інсталяція або портативне розпакування; служба та ярлики — за вибором |
| Debian / Ubuntu amd64 | `nyaaguard_*_amd64.deb` | Застосунок, Native Messaging і користувацька служба systemd |

**Актуальна версія 0.3.0:**

- [Завантажити для Windows x64](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.3.0/NyaaGuard-Setup-0.3.0-win-x64.exe) · [SHA-256](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.3.0/NyaaGuard-Setup-0.3.0-win-x64.exe.sha256)
- [Завантажити для Debian/Ubuntu amd64](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.3.0/nyaaguard_0.3.0_amd64.deb) · [SHA-256](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.3.0/nyaaguard_0.3.0_amd64.deb.sha256)

Кожен пакет має файл `.sha256`. Збірки поки не підписані комерційним сертифікатом, тому Windows SmartScreen може показати попередження.

## Оновлення та приватність

NyaaGuard щогодини перевіряє [`update-manifest.json`](../update-manifest.json), завантажує пакет через HTTPS і звіряє SHA-256. Основні перевірки локальні. URL надсилається до VirusTotal лише коли користувач додав API-ключ, адреси немає в локальних базах і онлайн-перевірка увімкнена.

> [!NOTE]
> Розширення Firefox ще розробляється і не входить до опублікованих випусків.

## Підтримати проєкт

| Мережа | Адреса |
|---|---|
| USDT — TRC20 | `TR3fkALFRTDyRaHsDU8aUmANGPRDy2gU1s` |
| ETH — ERC20 | `0x9d20248c779dcb742f7795a0c7461346c0c8934e` |
| BTC | `1BQwypiKfhNGb1ryKzdp7TBPL4wR6ckU4J` |
| PayPal | `spirt51@hotmail.com` |

Перед переказом криптовалюти обов’язково перевірте мережу й адресу.

- **[Журнал змін](CHANGELOG.uk.md)**
- **[Повідомити про помилку](https://github.com/Spirt51/NyaaGuard-Releases/issues)**
- **[Усі випуски](https://github.com/Spirt51/NyaaGuard-Releases/releases)**
