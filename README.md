# Zenfinity - адаптивное Web-приложение с бесконечной лентой публикаций

Разработано на межрегиональном хакатоне TulaHack 2.0 Accelerator в рамках решения кейса №15

Работает на ReactJS и получает посты в JSON формате из сервиса [JSONPlaceholder](https://jsonplaceholder.typicode.com/posts)

## Требования к приложению:
1. Публикации сортируются по некоторым правилам и не должны повторяться
2. Важно оптимизировать загрузку и отображение элементов ленты
3. Пользовательское взаимодействие с публикациями (лайки, комментарии и т.п.) можно делать по аналогии с российскими и зарубежными контент платформами (например, ВКонтакте, Instagram)

## Для сортировки публикаций мы использовали следующие правила:
1. Сначала посты сортируются по дате публикации, от самых новых к самым старым.
2. Затем посты сортируются по рейтингу, который можно вычислять на основе лайков, комментариев и просмотров. 
Примерная формула: rating = likes * 0.5 + comments * 0.3 + views * 0.2. Чем выше рейтинг, тем выше пост в ленте.
3. Наконец, проверяем, не повторяются ли посты в ленте. Если пост уже был показан, он пропускается и берется следующий по рейтингу.

## Как запустить приложение?
1. Выполните клонирование репозитория: \
   `git clone https://github.com/PRO100BYTE/zenfinity`
2. Установите зависимости: \
   `npm install`
3. Запустите сервер разработки: \
   `npm start`

## Скринкаст с демонстрацией интерфейса приложения
<video width="630" height="300" src="https://raw.githubusercontent.com/PRO100BYTE/zenfinity/main/screencast.mov"></video>
