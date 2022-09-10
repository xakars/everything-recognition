# everything-recognition

Скрипт позволяет распозновать в реальном времени объекты на видео, полученное через
веб камеру. Используется open source библиотека компьютерного зрения - OpenCV

Команда для установки зависимостей:
```console
pip install -r requirements.txt
```
Запускать скрипт командой:
```console
python run.py
```
### Описание 

В файле `config.py` можно настроить поведение распознавания.
В словарь CASCADES необходимо добавить объект, который необходимо распознать:
```code
CASCADES = {
    "Face profile": {
            "path": "haarcascades/faces/haarcascade_profileface.xml",
            "color": (255, 0, 0),
            "draw": True
    }
}
```
Где параметр "path" путь до данных в папке `haarcascades`, где представлены объекты, которые умеет распозновать 
скрипт. Также можно задать рамку распознанного объкта в формате rgb, параметром `color`.

Выход из скрипта осуществляется клавишей `q`.
