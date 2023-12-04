Описание
=
Данный проект скачивает фото с сайтов NASA, Space-X

Установка
=

```pip install -r requirements.txt```

Переменные окружения
=
Для настройки переменных окружения нужно создать файл .env указать там переменную окружения с токеном ```NASA_TOKEN=токен```
```TG_TOKEN=токен```

Ключ API.  Ключ API NASA можно получить в кабинете  [Сайт NASA](https://api.nasa.gov/)
Зарегистрировать бота и получить токен  [Как регистрировать бота](bit.ly/47ELQuZ)


Инструкция
=

```python3 fetch_spacex_images.py``` ссылка - скачивает фотографии запусков SpaceX
```python3 apod.py ссылка``` - скачивает фотографии с сайта NASA
```python3 nasa_earth.py``` ссылка - скачивает фотографии Земли

download_picture.py - функция для скачивание фотографий в директории
get_extention.py - забирает расширение файла
```python3 telegram_bot.py``` количество секунд - устанавливает необходимое количество секунд отправки файла в ТГ бота, если пусто, то задержка 4 часа. Если фотографии в директории заканчиваются, то меняется их порядок и отправляются заново

Примеры запуска скриптов
=

```$ python3 telegram_bot.py 50``` - задержка между публикациями 50 секунд

```$ python3 apod.py https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY``` - скачивание фото дня с сайта [NASA[(https://api.nasa.gov/)

```$ python3 fetch_spacex_images.py https://api.spacexdata.com/v5/launches/5eb87d47ffd86e000604b38a``` скачивает фото с запуска по Id

```$ python3 nasa_earth.py  https://api.nasa.gov/EPIC/archive/natural/2019/05/30/png/epic_1b_20190530011359.png?api_key=DEMO_KEY``` скачивает фото Земли с сайта [NASA](https://api.nasa.gov/)
