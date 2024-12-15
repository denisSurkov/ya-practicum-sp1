# Задание 1

## Уровень 1. Проектирование

В качестве фреймворка для работы с микрофрондендами я выбрал `Webpack Module Federation`. Весь проект построен с использованием `react`, следовательно можно указать в `shared` зависимость `react`. 

Общий токен для аутентификации проставлял бы в `secure` куках.

Запуск должен работать от приложения `host`, где будет описана общая структура приложения со ссылками на `remote` модули.

## Уровень 2. Планирование изменений

### `host`

Единая точка входа в приложение. Здесь же, или в отдельной библиотеке общих компонентов, стоит оставить шрифты, футер, хедер, вспомогательные компоненты, общую часть `css`.

### `auth`

Работа с входом, регистрацией пользователя. 

Компоненты:
- `Login`;
- `Register`.

В качестве api нужно использовал бы код из файла `auth.js`.

### `profile`

Работа с профилем пользователя. Отображение, изменение профиля.

Компоненты:
- `EditAvatarPopup`;
- `EditProfilePopup`;
- +`ProfileCard` - я бы еще добавил сам компонент с описанием профиля. Сейчас это часть компонента `Main`.

Необходимые api методы для работы:
- `setUserAvatar`;
- `setUserInfo`;
- `getUserInfo`.

### `cards`

Работа с фотокарточками. 

Компоненты:
- `AddPlacePopup`;
- `Card`;
- `ImagePopup`.

Необходимые api методы для работы:
- `changeLikeCardStatus`;
- `addCard`;
- `removeCard`;
- `getCardList`.


# Задание 2

