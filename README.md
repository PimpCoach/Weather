Погодное приложение, которое получает данные о погоде через API и отображает их пользователю.

В файле `config.yaml` необходимо:
В `API_KEY` нужно заменить на свой `API` с сайта https://openweathermap.org/
В `CITY` нужно заменить на свой город

Чтобы упаковать приложение в исполняемый файл (EXE), выполните следующие шаги:

1. Убедитесь, что вы находитесь в корневой директории вашего проекта, где находится ваш основной файл приложения.
2. Запустите команду:
3. 
```bash
pyinstaller --onefile --noconsole --hidden-import plyer.platforms.win.notification <название файла.py>
```
- `--onefile`: Указывает PyInstaller собрать все в один исполняемый файл.
- `--noconsole`: Отключает консольное окно при запуске приложения (полезно для графических приложений).
- `--hidden-import plyer.platforms.win.notification`: Указывает на необходимость включения модуля plyer для работы с уведомлениями в Windows.

После выполнения этой команды в папке `dist` будет создан исполняемый файл погодного уведомления. Так же необходимо положить файл `config.yaml` рядом с исполняемым файлом. Вы можете запускать его на любом компьютере без необходимости установки Python или зависимостей.

