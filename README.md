# cucumerCasinoTest

Для запуска автоматизированных GUI тестов необходимо предварительно выполнить следюущие обязательные шаги:

- должен быть установлен gradle последней версии https://gradle.org/install/, в переменную окружения PATH должен быть добавлен путь до gradle.bat
- должен быть установлен бразуер firefox или/и chrome последней версии
- должен быть скачен драйвер взаимодействия с установленной версией бразуера firefox - geckodriver, см. https://github.com/mozilla/geckodriver. В переменную окружения PATH должен быть добавлен путь до geckodriver.exe
- должен быть скачен драйверы взаимодействия с установленной версией бразуера chrome - chromedriver, см. https://chromedriver.chromium.org/. В переменную окружения PATH должен быть добавлен путь до chromedriver.exe

Для того чтобы запустить автоматизированные gui тесты необходимо выполнить команду:

- gradle clean test

Значения по умолчанию:

- browser - firefox (по умолчанию тесты запукаются с помощью браузера firefox)

Если нужно изменить значение по умолчанию (параметризовать значение выше) то нужно выполнить команду gradle clean test с соответствущими изменяемыми параметрами (название параметра должно начинаться с D), например:

- gradle clean test -Dbrowser=chrome

Информация о результате прогона тестов будет доступна в файле отчета target\cucumber-reports\index.html. В случае, если тест будет не пройдет то в отчет будут доступны скриншоты окна браузера после проваленного теста. Например:

- успешный прогон http://joxi.ru/KAxMeBzCZBMj0r
- прогон с ошибкой http://joxi.ru/L21JL60hRZ8xpA
