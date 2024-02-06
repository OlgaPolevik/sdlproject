
Создаем проект SDL
1.Устанавливаем библиотеку
2.в папку проекта линкуем или копируем файлы библотеки
3.создаем срр файл и переходим в VS Code
4.настраиваем сmake, debug  и CMakeLists.txt 

EMSDK подключен по этому примеру

https://floooh.github.io/2023/11/11/emscripten-ide.html

Пример с изображением взят отсюда

https://terminalroot.com/how-to-transform-your-games-into-c-cpp-for-the-web-with-emscripten-sdl2/

Есть еще старый срр файл, там тоже рабочий пример без изображения


На данный момент файлы создаются но при запуске html файла в браузере ничего не отображается,
А при запуске js файла выдается следующая ошибка:
/Users/olga/projects/sdlproject/build/debug/sdlproject.js:128
      throw ex;
      ^

ReferenceError: screen is not defined
    at _emscripten_get_screen_size (/Users/olga/projects/sdlproject/build/debug/sdlproject.js:6245:30)
    at sdlproject.wasm.Emscripten_VideoInit (wasm://wasm/sdlproject.wasm-00d743f2:wasm-function[1078]:0x77abe)
    at sdlproject.wasm.SDL_VideoInit (wasm://wasm/sdlproject.wasm-00d743f2:wasm-function[1087]:0x782ad)
    at sdlproject.wasm.SDL_InitSubSystem (wasm://wasm/sdlproject.wasm-00d743f2:wasm-function[260]:0x3abb)
    at sdlproject.wasm.SDL_Init (wasm://wasm/sdlproject.wasm-00d743f2:wasm-function[262]:0x3e51)
    at sdlproject.wasm.main (wasm://wasm/sdlproject.wasm-00d743f2:wasm-function[236]:0x308b)
    at /Users/olga/projects/sdlproject/build/debug/sdlproject.js:689:14
    at callMain (/Users/olga/projects/sdlproject/build/debug/sdlproject.js:9849:15)
    at doRun (/Users/olga/projects/sdlproject/build/debug/sdlproject.js:9899:23)
    at run (/Users/olga/projects/sdlproject/build/debug/sdlproject.js:9914:5)

Node.js v18.16.1


На других примерах выдавалась та же ошибка!

Файлы без использования сдл формируются корректно
Примеры сдл которые выполняются без использования emsdk тоже компилируются в корректный исполняемый файл 