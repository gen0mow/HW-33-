Проект предназначен для тестирования авторизации на сайте https://b2c.passport.rt.ru/auth/.
Тесты покрывают функционал авторизации/регистрации/восстановления пароля
Инструменты:

- Selenium: Используется для автоматизации браузера и взаимодействия с веб-страницами.
- Pytest: Применяется для управления тестами, обеспечения их структуры и удобного вывода результатов.
  
Данные инструменты были выбраны т.к.:

1. Selenium: 
   - Выбран за свою возможность эмулировать действия пользователя в браузере и проверять, как веб-приложение реагирует на различные пользовательские действия.
   
2. Pytest: 
   - Предпочтён благодаря своей простоте в написании тестов и возможности использовать фикстуры.

В тестах проверялось:

- Авторизация:
  - Проверка успешной авторизации с использованием номера телефона, электронной почты, логина и лицевого счета.
  - Проверка обработки ситуаций с неверными данными входа.

- Восстановление пароля:
  - Тесты на восстановление пароля через номер телефона и электронную почту.
  
- Регистрация:
  - Проверка успешной регистрации.
  - Проверка обработки ситуаций с неверными данными для регистрации.
    
- Двухфакторная аутентификация:
  - Тестирование авторизации с использованием кода, отправленного на телефон или по электронной почте.

Что сделано:

1. Тесты для авторизации:
   - Успешная авторизация с правильными данными (номер телефона, email, логин).
   - Неуспешная авторизация с неправильными данными.

2. Тесты восстановления пароля:
   - Проверка функциональности восстановления пароля через телефон и email.

3. Тесты для регистрации:
   - Проверка успешной регистрации и обработка ошибок при вводе некорректных данных.

4. Тесты двухфакторной аутентификации:
   - Проверка авторизации с использованием SMS-кода и обработка ошибок при неправильном коде.
  
Техники тестирования которые были применены:

1. Функциональное тестирование:
   - Проверка основных функций веб-приложения, таких как авторизация, сброс пароля и регистрация, через различные способы входа (номер телефона, email, логин).

2. Тестирование на корректность ввода (ввод данных):
   - Проверка обработки как валидных, так и невалидных данных входа, чтобы убедиться в правильности ответов системы на разные сценарии.

3. Тестирование пользовательского интерфейса (UI тестирование):
   - Проверка элементов интерфейса, таких как кнопки, поля ввода и сообщения об ошибках, для обеспечения их корректного отображения и функциональности.

4. Негативное тестирование:
   - Проверка системы на поведение при вводе некорректных данных и оценка обработки ошибок, чтобы убедиться, что приложение корректно сообщает об ошибках.
  
Запуск тесто осуществляется командой в консоль:

    pytest -v --driver Chrome --driver-path /path/to//chromedriver.exe test_HW33.py
    
  Где /path/to/ ваш путь для веб-драйвера (В моем случае запуск осуществлялся командой: python -m pytest -v --driver Chrome --driver-path C:\chromedriver.exe test_HW33.py)
    
