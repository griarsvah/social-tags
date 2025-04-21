# social-tags
social-meta-tags

## twitter
<!-- Уникальные Twitter Card-теги (не дублируются в Open Graph) -->
### 1. twitter:card
Тип карточки, которая будет отображаться. Примеры:
summary — стандартная карточка с заголовком, описанием и изображением.
summary_large_image — карточка с большим изображением.
player — карточка для видео или аудио.
app — карточка для мобильного приложения.
product — карточка для товаров с ценой и доступностью.
```html
<meta name="twitter:card" content="summary_large_image">
```

### 2. twitter:title
Заголовок страницы, который будет отображаться в карточке. Пример:
```html
<meta name="twitter:title" content="Заголовок страницы">
```

### 3. twitter:description
Описание страницы, которое будет отображаться в карточке. Пример:
```html
<meta name="twitter:description" content="Описание страницы">
```

### 4. twitter:image
URL изображения, которое будет отображаться в карточке. Пример:
```html
<meta name="twitter:image" content="URL_картинки">
```

### 5. twitter:image:alt
Описание изображения (для доступности). Пример:
```html
<meta name="twitter:image:alt" content="Описание изображения">
```

### 6. twitter:site
Указывает аккаунт Twitter, с которым связан сайт. Пример:
```html
<meta name="twitter:site" content="@имя_сайта">
```

### 7. twitter:player
```html
<meta name="twitter:player" content="https://example.com/video/embed">
```

### 8. twitter:player:width
```html
<meta name="twitter:player:width" content="1280">
```

### 9. twitter:player:height
```html
<meta name="twitter:player:height" content="720">
```

### 10. twitter:creator
Указывает аккаунт Twitter автора контента. Пример:
```html
<meta name="twitter:creator" content="@автор_контента">
```

### 12. twitter:url
Указывает URL страницы. Пример:
```html
<meta name="twitter:url" content="https://example.com/page">
```

### 11. twitter:domain
Указывает домен сайта (обычно используется для улучшения SEO). Пример:
```html
<meta name="twitter:domain" content="example.com">
```

### 13. twitter:label1 и twitter:data1
Используются для отображения дополнительных данных в карточке (например, цена, доступность). Пример:
```html
<meta name="twitter:label1" content="Цена">
<meta name="twitter:data1" content="$19.99">
```

### 11. twitter:label2 и twitter:data2
Аналогичны тегам label1 и data1, но могут быть использованы для других данных (например, статус или другие характеристики). Пример:
```html
<meta name="twitter:label2" content="Статус">
<meta name="twitter:data2" content="В наличии">
```

### 12. twitter:app:name:iphone
Название приложения для iPhone. Пример:
```html
<meta name="twitter:app:name:iphone" content="MyApp">
```

### 13. twitter:app:id:iphone
Идентификатор приложения в App Store для iPhone. Пример:
```html
<meta name="twitter:app:id:iphone" content="123456789">
```

### 14. twitter:app:name:ipad
Название приложения для iPad. Пример:
```html
<meta name="twitter:app:name:ipad" content="MyApp">
```

### 15. twitter:app:id:ipad
Идентификатор приложения в App Store для iPad. Пример:
```html
<meta name="twitter:app:id:ipad" content="123456789">
```

### 16. twitter:app:name:googleplay
Название приложения для Android. Пример:
```html
<meta name="twitter:app:name:googleplay" content="MyApp">
```

### 17. twitter:app:id:googleplay
Идентификатор приложения в Google Play для Android. Пример:
```html
<meta name="twitter:app:id:googleplay" content="com.example.myapp">
```

### 18. twitter:app:url:iphone
URL приложения для iPhone, по которому его можно открыть. Пример:
```html
<meta name="twitter:app:url:iphone" content="myapp://">
```

### 19. twitter:app:url:ipad
```html
URL приложения для iPad, по которому его можно открыть. Пример:
<meta name="twitter:app:url:ipad" content="myapp://">
```

### 20. twitter:app:url:googleplay
URL приложения для Android, по которому его можно открыть. Пример:
```html
<meta name="twitter:app:url:googleplay" content="https://play.google.com/store/apps/details?id=com.example.myapp">
```

### 21. twitter:app:count
Количество взаимодействий с приложением или контентом в приложении. Пример:
```html
<meta name="twitter:app:count" content="true">
```

### 22. twitter:creator:label
Этот тег используется для указания типа контента, который может быть полезен в контексте карточки Twitter. Например, это может быть «Автор» или «Компания». Пример:
```html
<meta name="twitter:creator:label" content="Автор">
```

### 23. twitter:creator:data
Используется в паре с twitter:creator:label для передачи данных, например, имени или информации о компании. Пример:
```html
<meta name="twitter:creator:data" content="Иван Иванов">
```

### 24. twitter:publisher
Этот метатег аналогичен тегу twitter:site, но он используется для указания аккаунта Twitter, который является владельцем или издателем контента. Пример:
```html
<meta name="twitter:publisher" content="@имя_издателя">
```


### 25. twitter:tracking_id
Этот тег используется для отслеживания метаданных контента, например, для аналитики. Пример:
```html
<meta name="twitter:tracking_id" content="track12345">
```


---

# Метатеги для Apple приложений:

## 1. Universal Links:
Universal Links — это способ открытия приложений на устройствах iOS через стандартные HTTP(S) ссылки. Для их работы требуется добавить определенные метатеги, которые помогут операционной системе iOS корректно распознать ссылку и открыть приложение, если оно установлено.

### apple-app-site-association:
Этот файл размещается на сервере и необходим для того, чтобы Universal Links работали с вашим приложением. Это не HTML метатег, а файл JSON, который должен быть доступен по адресу https://example.com/apple-app-site-association.

Пример содержания:
```json
{
  "applinks": {
    "details": [
      {
        "appID": "TEAM_ID.com.example.app",
        "paths": ["/path/*"]
      }
    ]
  }
}
```

## 2. App Clips:
App Clips — это легковесные версии приложений, которые позволяют пользователям использовать части приложения без необходимости его скачивания. Для App Clips нужно указать несколько метатегов для облегчения взаимодействия с приложением.

### apple-app-id:
Указывает уникальный идентификатор приложения в App Store.
```html
<meta name="apple-app-id" content="1234567890">
```

### apple-app-name:
Указывает имя приложения, которое будет отображаться при интеракции с App Clips.
```html
<meta name="apple-app-name" content="Название приложения">
```

## 3. App Store метатеги:
Для того чтобы приложение корректно отображалось в App Store или в других местах экосистемы Apple, используются метатеги для того, чтобы указать информацию о приложении. Эти метатеги могут быть использованы на сайте, который продвигает приложение.

### apple-itunes-app:
Этот метатег используется для добавления ссылки на приложение в App Store и позволяет пользователю перейти в магазин, чтобы скачать приложение.
```html
<meta name="apple-itunes-app" content="app-id=1234567890">
```

## 4. Apple Smart App Banner:
Это метатег, который используется для отображения баннера в браузере Safari на мобильных устройствах iOS. Этот баннер предлагает пользователю скачать приложение, если оно еще не установлено, или открыть его, если оно уже установлено.

### apple-itunes-app:
Также используется для показа баннера на сайте. Пример:
```html
<meta name="apple-itunes-app" content="app-id=1234567890,affiliate-data=myAffiliateData">
```
app-id – ID приложения в App Store.
app-argument – deep link для открытия контента в приложении.
affiliate-data – партнерские данные (опционально).


3. Apple News & Apple Music
Для интеграции с Apple News и Apple Music используются Open Graph (og:) + специальные теги.
Пример для Apple News:
### apnl:title
### apnl:access
```html
<meta name="apnl:title" content="Заголовок статьи">
<meta name="apnl:access" content="free|subscription">
```

Пример для Apple Music (встраивание плеера):
### apple-music:url
```html
<meta name="apple-music:url" content="https://music.apple.com/album/123456789">
```

Дополнительные теги для Safari

## 6. Push Notifications:
Для взаимодействия с Push Notifications в приложении через браузеры Safari или другие сервисы можно использовать метатеги и атрибуты, такие как:


<!-- Обязательные для Apple -->
### apple-mobile-web-app-capable:
Этот метатег указывает, что ваше приложение должно быть способно работать в полноэкранном режиме без использования интерфейса браузера.
```html
<meta name="apple-mobile-web-app-capable" content="yes">
```

### apple-mobile-web-app-status-bar-style:
Определяет, как будет отображаться статус-бар на устройствах iOS.
```html
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
```

### apple-mobile-web-app-title
```html
<meta name="apple-mobile-web-app-title" content="Название приложения">
```



Вывод:
Для Apple приложений важны такие метатеги, как Universal Links (для связывания ссылок с приложением), App Clips, метатеги для App Store, а также Smart App Banner для отображения баннера в Safari.

Специфичные метатеги, такие как apple-itunes-app, apple-app-id и apple-app-name, используются для улучшения интеграции с экосистемой Apple.

Стандартные Open Graph метатеги также важны для социальных платформ Apple (iMessage, Apple News).


---


Уникальные социальные метатеги для Microsoft, которые используются в экосистеме Microsoft (LinkedIn, Microsoft Teams, Outlook, Bing, Windows Share и других сервисах):
Microsoft (для приложений в Windows Store)


### msapplication-TileColor
Цвет плитки в меню Пуск (Windows 8/10)
```html
<meta name="msapplication-TileColor" content="#2b5797">
```


### msapplication-tooltip
Подсказка при наведении на плитку
```html
<meta name="msapplication-tooltip" content="Microsoft Store">
```

### msapplication-starturl
URL, с которого начинается приложение
```html
<meta name="msapplication-starturl" content="/">
```

### msapplication-navbutton-color
Цвет панели навигации на Windows Phone
```html
<meta name="msapplication-navbutton-color" content="#2b5797">
```

### theme-color
Цвет окна/браузера
```html
<meta name="theme-color" content="#ffffff">
```

### viewport
Настройки адаптивной вёрстки
```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

### description
Описание страницы
```html
<meta name="description" content="Official page for the Microsoft Store app.">
```

---

1. LinkedIn (основной)
Хотя LinkedIn использует Open Graph (og:), у него есть специфичные рекомендации:
```html
<meta property="og:title" content="Заголовок">
<meta property="og:description" content="Описание">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:url" content="https://example.com">
<!-- Рекомендуется для LinkedIn -->
<meta property="og:type" content="article"> <!-- или "website" -->
<meta property="article:published_time" content="2023-01-01T00:00:00Z">
<meta property="article:author" content="Автор">
```
Особенности LinkedIn:
Предпочитает article: для новостей и блогов.
Требует абсолютных URL для изображений.
Минимальный размер изображения: 1200×627 px.

2. Microsoft Teams (встраивание ссылок)
Для красивого отображения ссылок в Teams:
<meta name="msapplication-TileColor" content="#FFFFFF">
<meta name="msapplication-TileImage" content="/mstile-144x144.png">
<!-- Для предпросмотра в Teams (использует Open Graph) -->
```html
<meta property="og:title" content="Заголовок в Teams">
<meta property="og:description" content="Описание для Teams">
<meta property="og:image" content="https://example.com/teams-preview.jpg">
```

3. Outlook (электронные письма)
Для корректного отображения ссылок в Outlook:
<!-- Управление превью в Outlook -->
```html
<meta name="x-ms-application-ID" content="MyApp">
<meta name="x-ms-application-PackageFamilyName" content="MyApp.Package">
```

4. Windows Share (для обмена через Win + H)
Windows использует Open Graph, но можно добавить:
### application-name
Имя приложения (в заголовках/иконках)
```html
<meta name="application-name" content="Microsoft Store">
```

### msapplication-config
Ссылка на файл browserconfig.xml (иконки, плитки и т.п.)
```html
<meta name="msapplication-config" content="/browserconfig.xml">
```


5. Bing (поисковая система)
Для улучшения сниппетов в Bing:
```html
<meta name="msvalidate.01" content="BING_VERIFICATION_CODE">
<meta name="robots" content="index,follow">
```

6. Skype (превью ссылок)
Skype также полагается на Open Graph, но можно уточнить:
```html
<meta property="skype:title" content="Заголовок для Skype">
<meta property="skype:description" content="Описание для Skype">
```html

7. Microsoft Clarity (аналитика)
Для интеграции с сервисом аналитики Clarity:
```html
<meta name="clarity-config" content="PROJECT_ID=YOUR_ID">
```

Проверка
LinkedIn: Post Inspector https://www.linkedin.com/post-inspector/

Bing: Webmaster Tools https://www.bing.com/webmasters/about

Teams/Outlook: Проверяется вручную в клиентах.

---

---



## Apple Touch Icon:
Для отображения иконки при добавлении сайта на главный экран устройства Apple используется специальный метатег. Этот метатег позволяет задавать иконку для сайтов, которая будет использоваться при создании ярлыка на главном экране в iOS.

<!-- Для иконок (Web Clip) -->
### apple-touch-icon
Иконка для добавления на главный экран.
```html
<link rel="apple-touch-icon" href="https://example.com/apple-icon.png">
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon-180x180.png">
<link rel="apple-touch-startup-image" href="/launch.png">
```

<!-- Отключение автоматического определения и форматирования телефонных номеров -->
<meta name="format-detection" content="telephone=no">

## Apple News метатеги:
Для Apple News можно использовать специфические метатеги для улучшенной презентации контента в новостных лентах Apple.

### apple-news-title
Заголовок новости.
```html
<meta name="apple-news-title" content="Заголовок новости">
```

### apple-news-description
Описание новости.
```html
<meta name="apple-news-description" content="Описание новости">
```

### apple-news-image
Изображение для отображения в ленте новостей.
```html
<meta name="apple-news-image" content="https://example.com/news-image.jpg">
```



---




Специфичные метатеги для Google:
уникальные социальные метатеги для Google
для улучшения отображения контента в поисковой выдаче, почте Gmail, Google Chat и других сервисах экосистемы Google:

```html
<!-- Для авторов (использовалось в Google+) -->
<link rel="author" href="https://plus.google.com/[ID_профиля]">
<link rel="publisher" href="https://plus.google.com/[ID_страницы]">
```

6. Google Аналитика / Tag Manager
Для интеграции с сервисами аналитики:
```html
<!-- Google Analytics -->
<meta name="google-analytics" content="GA_MEASUREMENT_ID">

<!-- Google Tag Manager -->
<meta name="google-tag-manager" content="GTM-XXXXXX">
```
7. Ускоренные мобильные страницы (AMP)
```html
<!-- Компоненты AMP -->
<script async src="https://cdn.ampproject.org/v0.js"></script>
```

9. Google Поиск Картинок
Для оптимизации изображений:
```html
<meta name="image" content="https://example.com/image.jpg">
<link rel="image_src" href="https://example.com/image.jpg">
```

### google:title
Заголовок, который будет отображаться в результатах поиска Google.
```html
<meta name="google:title" content="Заголовок страницы">
```

### google:description
Описание страницы, которое будет отображаться в результатах поиска.
```html
<meta name="google:description" content="Описание страницы">
```

### google:image
URL изображения, которое будет отображаться в поисковых результатах Google.
```html
<meta name="google:image" content="https://example.com/image.jpg">
```

### google:site_name
Название сайта для отображения в результатах поиска.
```html
<meta name="google:site_name" content="Название сайта">
```

### google:keywords
Ключевые слова для страницы, которые Google использует для поиска (хотя Google больше не использует этот метатег для ранжирования).
```html
<meta name="google:keywords" content="ключевое слово, ещё одно ключевое слово">
```

### google:robots
Инструкция для роботов поисковых систем, например, для индексации или исключения из индексации.
```html
<meta name="google:robots" content="index, follow">
```

### google:author
Автор страницы или контента.
```html
<meta name="google:author" content="Имя автора">
```

### google:publisher
Информация о владельце контента или паблишере, например, имя компании.
```html
<meta name="google:publisher" content="Имя компании или издателя">
```

### google:date
Дата публикации страницы.
```html
<meta name="google:date" content="2025-04-17">
```

### google:robots
Указывает поисковому роботу, что делать с этим контентом (индексировать или нет).
```html
<meta name="robots" content="index, follow">
```

Другие метатеги для улучшения индексации в Google:
### robots — Стандартный метатег, который сообщает Google, должен ли контент быть проиндексирован.
```html
<meta name="robots" content="noindex, nofollow">
```

### google:lang — Язык страницы, который используется для улучшения поиска по языковым настройкам.
```html
<meta name="google:lang" content="ru">
```

Структурированные данные для Google:
### Schema.org метки, которые помогают улучшить отображение в поисковой выдаче (например, рейтинг, события, товары).
```html
<!-- Схема JSON-LD (предпочтительный формат для Google) -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Заголовок статьи",
  "description": "Описание статьи",
  "image": "https://example.com/image.jpg",
  "author": {
    "@type": "Person",
    "name": "Автор"
  },
  "datePublished": "2023-01-01"
}
</script>
```

Проверка
Rich Snippets: Google Testing Tool https://search.google.com/test/rich-results

AMP: AMP Validator https://validator.ampproject.org/

Gmail: Проверяется вручную, отправляя письмо себе.



----



## Метатеги для Telegram:
Стандартные Open Graph метатеги +
Специфичные метатеги для Telegram:

```html
<meta name="telegram:channel" content="@channelusername">
<meta name="telegram:domain" content="example.com">
```
```html
<link rel="alternate" href="https://t.me/iv?url=https://example.com&rhash=ABC123">
<meta property="al:android:url" content="tg://resolve?domain=telegram&post=123">
<meta property="al:ios:url" content="tg://resolve?domain=telegram&post=123">
```

### telegram:title
Заголовок для отображения в Telegram.
```html
<meta property="telegram:title" content="Заголовок ссылки">
```

### telegram:description
Описание, которое будет отображаться в ссылке.
```html
<meta property="telegram:description" content="Описание контента">
```

### telegram:image
Изображение, которое будет отображаться в карточке при отправке ссылки.
```html
<meta property="telegram:image" content="https://example.com/image.jpg">
```

### telegram:audio
URL аудио-файла, который будет прикреплен к ссылке (если применимо).
```html
<meta property="telegram:audio" content="https://example.com/audio.mp3">
```

### telegram:video
URL видео, которое будет прикреплено к ссылке (если применимо).
```html
<meta property="telegram:video" content="https://example.com/video.mp4">
```

### telegram:source
Источник контента, например, веб-сайт или блог.
```html
<meta property="telegram:source" content="https://example.com">
```

### telegram:creator
Указывает создателя или автора контента.
```html
<meta property="telegram:creator" content="Автор контента">
```

7. Проверка превью
Проверить отображение можно:

Отправив ссылку в любой Telegram-чат 

Через официального бота https://t.me/WebpageBot

В Telegram Web https://web.telegram.org/


---



## Специфичные метатеги для Slack:

### slack:channel
Указывает канал, в который ссылка будет опубликована в Slack.
```html
<meta property="slack:channel" content="#general">
```

### slack:message
Указывает текст сообщения, которое будет прикреплено к ссылке.
```html
<meta property="slack:message" content="Не забудьте прочитать эту статью!">
```

### slack:mention
Указывает, кого нужно упомянуть в сообщении (например, @channel, @everyone).
```html
<meta property="slack:mention" content="@channel">
```

6. Как обновить превью в Slack
Если Slack показывает устаревшее превью:

Добавьте параметр ?slack=1 к URL

Или используйте команду /unfurl url в Slack-чате

Или очистите кэш через /unfurl clear

7. Проверка превью
Проверить отображение можно:

Отправив ссылку в любой Slack-чат

Используя Slack API для unfurl https://api.slack.com/reference/messaging/link-unfurling

Через тестовое рабочее пространство https://slack.com/get-started#/create

---


### youtube:video
Это метатег, указывающий URL видео на YouTube.
```html
<meta property="youtube:video" content="https://www.youtube.com/watch?v=video_id">
```

### youtube:channel
Указывает канал, на котором размещено видео.
```html
<meta property="youtube:channel" content="https://www.youtube.com/c/channel_name">
```

### youtube:duration
Указывает продолжительность видео в секундах.
```html
<meta property="youtube:duration" content="240">
```

### youtube:category Категория видео (например, музыка, развлечение и т.д.).
```html
<meta property="youtube:category" content="Music">
```

### youtube:tags Теги, связанные с видео (через запятую).
```html
<meta property="youtube:tags" content="tag1, tag2, tag3">
```

### youtube:views Количество просмотров видео.
```html
<meta property="youtube:views" content="1000000">
```

### youtube:published Дата публикации видео.
```html
<meta property="youtube:published" content="2025-04-17T10:00:00Z">
```

### youtube:likes Количество лайков на видео.
```html
<meta property="youtube:likes" content="10000">
```

### youtube:dislikes Количество дизлайков на видео.
```html
<meta property="youtube:dislikes" content="100">
```

### youtube:comment_count Количество комментариев к видео.
```html
<meta property="youtube:comment_count" content="500">
```

4. Особые случаи
Для YouTube Music:
```html
<meta name="youtube:music:album" content="ALBUM_ID">
<meta name="youtube:music:artist" content="ARTIST_NAME">
```

### youtube:kids
Для YouTube Kids:
```html
<meta name="youtube:kids" content="true">
```

### youtube:live Указывает, является ли видео трансляцией.
Для Live-стримов:
```html
<meta property="youtube:live" content="true">
<meta name="youtube:liveStart" content="2023-01-01T18:00:00Z">
<meta name="youtube:liveEnd" content="2023-01-01T20:00:00Z">
```

### youtube:quality Качество видео (например, 720p, 1080p, и т.д.).
```html
<meta property="youtube:quality" content="1080p">
```

### youtube:thumbnail URL изображения миниатюры видео.
```html
<meta property="youtube:thumbnail" content="https://www.youtube.com/thumbnail.jpg">
```

5. Важные нюансы
youtube:video – обязателен для корректного отображения в YouTube API
og:video:url должен содержать embed-ссылку (не watch?v=)
Для Shorts используйте вертикальные размеры (720x1280)
Все даты – строго в формате ISO 8601



6. Проверка и валидация
Rich Results Test от Google:
https://search.google.com/test/rich-results

Twitter Card Validator:
https://cards-dev.twitter.com/validator

Facebook Sharing Debugger:
https://developers.facebook.com/tools/debug/

6. Проверка
YouTube Data API:
https://www.googleapis.com/youtube/v3/videos?id=VIDEO_ID&part=snippet&key=YOUR_API_KEY

---


```html
<meta name="pinterest:media" content="https://example.com/pin-image.jpg">
<meta name="pinterest:creator" content="@yourpinterest">
<meta name="pinterest:type" content="article">
```

```html
<!-- Для Product Pins -->
<meta property="product:price:amount" content="49.99">
<meta property="product:price:currency" content="USD">
<meta property="product:availability" content="in stock">
<meta property="product:brand" content="Название бренда">
```

Рецепты (Recipe Pins)
```html
<meta property="og:type" content="recipe">
<meta property="recipe:prep_time" content="PT15M">
<meta property="recipe:cook_time" content="PT30M">
<meta property="recipe:ingredient" content="1 чашка муки">
```

### 1. pinterest:description
Описание контента, которое будет отображаться на Pinterest при репосте. Пример:
```html
<meta property="pinterest:description" content="Описание контента для Pinterest">
```

### 2. pinterest:image
URL изображения, которое Pinterest будет использовать для пина. Пример:
```html
<meta property="pinterest:image" content="https://example.com/image.jpg">
```

### 3. pinterest:title
Заголовок пина, который будет использоваться при публикации контента на Pinterest. Пример:
```html
<meta property="pinterest:title" content="Заголовок пина">
```

### 4. pinterest:source
Источник контента, который может быть полезен для авторов и бизнеса. Пример:
```html
<meta property="pinterest:source" content="https://example.com">
```

### 5. pinterest:video
URL видео, которое будет использоваться при размещении контента с видео на Pinterest. Пример:
```html
<meta property="pinterest:video" content="https://example.com/video.mp4">
```

### 6. pinterest:audio
URL аудио-файла, который будет связан с контентом. Пример:
```html
<meta property="pinterest:audio" content="https://example.com/audio.mp3">
```

### 7. pinterest:card
Этот метатег используется для указания типа карточки, которую Pinterest будет использовать при отображении пина. Пример:
```html
<meta property="pinterest:card" content="summary_large_image">
```

### 8. pinterest:creator
Указывает имя автора или создателя контента. Это может быть полезно для брендов и авторов, чтобы указать, кто создал контент. Пример:
```html
<meta property="pinterest:creator" content="Автор контента">
```

### 9. pinterest:section
Указывает категорию или раздел, к которому относится контент. Это может помочь организовать контент в Pinterest. Пример:
```html
<meta property="pinterest:section" content="Lifestyle">
```


Особенности изображений:
Оптимальный размер: 1000x1500 px (соотношение 2:3)
Форматы: JPEG или PNG
Максимальный размер файла: 20MB

Рекомендации:
```html
<!-- Альтернативные изображения -->
<link rel="preload" href="https://example.com/pin-image.jpg" as="image">
<!-- Ленивая загрузка -->
<meta name="pinterest:lazy" content="true">
```html
6. Проверка и валидация
Rich Pins Validator:
https://developers.pinterest.com/tools/url-debugger/

Pinterest Webmaster Tools:
https://www.pinterest.com/settings/claim

7. Важные рекомендации
Всегда используйте высококачественные вертикальные изображения
Добавьте текстовое описание в атрибут alt для изображений
Для товаров укажите актуальную цену и наличие
Используйте Schema.org разметку для лучшей индексации


---



### 1. og:title
Заголовок страницы. Пример:
```html
<meta property="og:title" content="Заголовок страницы">
```

### 2. og:type
Тип контента (например, website, article, video, music, и т. д.). Пример:
```html
<meta property="og:type" content="website">
```

### 3. og:image
URL изображения, которое будет использоваться в карточке. Пример:
```html
<meta property="og:image" content="https://example.com/image.jpg">
```

###  4. og:image:secure_url
URL изображения через HTTPS. Пример:
```html
<meta property="og:image:secure_url" content="https://example.com/image.jpg">
```

### 5. og:image:type
Тип изображения (например, image/jpeg или image/png). Пример:
```html
<meta property="og:image:type" content="image/jpeg">
```

### 6. og:image:width
Ширина изображения. Пример:
```html
<meta property="og:image:width" content="1200">
```

### 7. og:image:height
Высота изображения. Пример:
```html
<meta property="og:image:height" content="630">
```

### 8. og:url
URL страницы, который будет использоваться в Open Graph карточке. Пример:
```html
<meta property="og:url" content="https://example.com/page">
```

### 9. og:description
Описание страницы, которое будет отображаться в карточке. Пример:
```html
<meta property="og:description" content="Описание страницы">
```

### 10. og:site_name
Название сайта (например, название вашей компании или бренда). Пример:
```html
<meta property="og:site_name" content="Example Site">
```

### 11. og:locale
Локализация страницы (например, en_US для английского языка). Пример:
```html
<meta property="og:locale" content="en_US">
```

### 12. og:determiner
Определитель, который используется перед названием (например, "a", "an", "the"). Пример:
```html
<meta property="og:determiner" content="the">
```

### 13. og:audio
URL аудио-файла (если контент связан с аудио). Пример:
```html
<meta property="og:audio" content="https://example.com/audio.mp3">
```

### 14. og:audio:secure_url
URL аудио-файла через HTTPS. Пример:
```html
<meta property="og:audio:secure_url" content="https://example.com/audio.mp3">
```

### 15. og:video
URL видео (если контент связан с видео). Пример:
```html
<meta property="og:video" content="https://example.com/video.mp4">
```

### 16. og:video:secure_url
URL видео через HTTPS. Пример:
```html
<meta property="og:video:secure_url" content="https://example.com/video.mp4">
```

### 17. og:video:type
Тип видео (например, video/mp4). Пример:
```html
<meta property="og:video:type" content="video/mp4">
```

### 18. og:video:width
Ширина видео. Пример:
```html
<meta property="og:video:width" content="1200">
```

### 19. og:video:height
Высота видео. Пример:
```html
<meta property="og:video:height" content="630">
```

### 20. og:audio:type
Тип аудио-файла (например, audio/mpeg). Пример:
```html
<meta property="og:audio:type" content="audio/mpeg">
```

### 21. og:updated_time
Время последнего обновления страницы. Пример:
```html
<meta property="og:updated_time" content="2025-04-17T12:00:00Z">
```

### 22. og:locale:alternate
Дополнительные локализации, если страница доступна на других языках. Пример:
```html
<meta property="og:locale:alternate" content="es_ES">
```

### 23. og:video:tag
Теги, связанные с видео. Пример:
```html
<meta property="og:video:tag" content="тег1, тег2">
```


### 24. fb:app_id
Идентификатор приложения Facebook, если вы хотите привязать контент к своему приложению Facebook. Пример:
```html
<meta property="fb:app_id" content="1234567890">
```

### 25. og:place
Указывает местоположение, связанное с контентом. Это может быть полезно, например, для ресторанов или других локальных бизнесов. Пример:
```html
<meta property="og:place" content="https://www.example.com/place">
```

### 26. og:country_name
Указывает страну, связанное с контентом. Пример:
```html
<meta property="og:country_name" content="Россия">
```

### 27. og:street-address
Указывает конкретный адрес (например, для бизнеса или организации). Пример:
```html
<meta property="og:street-address" content="123 Примерная улица">
```

### 28. og:locality
Указывает город или населенный пункт, связанный с контентом. Пример:
```html
<meta property="og:locality" content="Москва">
```

### 29. og:region
Указывает регион или область, связанное с контентом. Пример:
```html
<meta property="og:region" content="Центральный федеральный округ">
```

### 30. og:postal-code
Указывает почтовый индекс для местоположения. Пример:
```html
<meta property="og:postal-code" content="123456">
```




---

1. Базовые метатеги для Yahoo! Search
```html
<!-- Язык контента -->
<meta http-equiv="content-language" content="ru">

<!-- Автор и копирайт -->
<meta name="author" content="Ваше Имя">
<meta name="copyright" content="Название компании">

<!-- Гео-метки -->
<meta name="geo.region" content="RU-MOW">
<meta name="geo.placename" content="Москва">
<meta name="geo.position" content="55.7558;37.6176">
<meta name="ICBM" content="55.7558, 37.6176">
```

2. Уникальные метатеги Yahoo!
Эти теги работают только в экосистеме Yahoo:
```

```html
<!-- Версия сайта для Yahoo! -->
<meta name="y_key" content="YAHOO_VERIFICATION_KEY">

<!-- Для Yahoo! Site Explorer -->
<meta name="yahoo:validate" content="YAHOO_VALIDATION_TOKEN">

<!-- Для Yahoo! News -->
<meta name="yahoo:news" content="category=technology;language=ru">

<!-- Для Yahoo! Shopping -->
<meta name="yahoo:product" content="category=electronics;price=299.99">
```

3. Метатеги для Yahoo! Mail
Для корректного отображения писем:
```html
<!-- Отключение автоформатирования -->
<meta name="yahoo:format-detection" content="telephone=no">

<!-- Специальные стили для Yahoo Mail -->
<meta name="yahoo:styledmail" content="true">
<style type="text/css" yahoo="fix">
  /* CSS-стили для Yahoo Mail */
</style>
```



5. Особые случаи
Для Yahoo! Answers:
```html
<meta name="yahoo:answers:category" content="Компьютеры и Интернет">
<meta name="yahoo:answers:type" content="Вопрос">
```

Для Yahoo! Finance:
```html
<meta name="yahoo:finance:ticker" content="AAPL">
<meta name="yahoo:finance:currency" content="USD">
```

Для Yahoo! Weather:
```html
<meta name="yahoo:weather:location" content="Москва,Россия">
<meta name="yahoo:weather:unit" content="c">
```

6. Проверка и валидация
Yahoo! Site Explorer:
(сервис закрыт, используйте Yahoo Webmaster Tools)https://login.yahoo.com/

Проверка email-верстки:
Litmus https://www.litmus.com/ или Email on Acid https://www.emailonacid.com/

7. Важные рекомендации
Для Yahoo! Search используйте классические SEO-метатеги
Гео-метки особенно важны для локального поиска
Для Yahoo! Mail всегда добавляйте инлайновые стили
Используйте Yahoo! Webmaster Tools для мониторинга
