---
title: "AidenLx's Folder Note"
---

# AidenLx's Folder Note

## Установка

### Ссылка на ручную установку

<https://github.com/aidenlx/alx-folder-note/>

### Автоматическая установка

Доступна из меню `Community plugins` (`Сторонние плагины`) `Obsidian`, плагин находится по названию `AidenLx's Folder Note`.

После установки плагина и его активации, в окне настроек плагина `AidenLx's Folder Note` будет отображаться сообщение об отсутствии в программе `Obsidian` плагина `Folder Note Core` и будет предложено установить его по нажатию на кнопку, без этого дополнительного плагина `AidenLx's Folder Note` работать не будет. Установите предложенный плагин и активируйте его, после чего появятся и станут доступны настройки `AidenLx's Folder Note`. Для начала использования все настройки можно оставить по-умолчанию.

## Краткое описание

Add description, summary and more info to folders with folder notes.

Плагин позволяет добавить к папке описание хранящихся в ней файлов и другую информацию, которая будет храниться в т.н. `заметке-внутри-папки` (`folder note`).

## Функционал

После установки и включения плагин позволяет создать `заметку-внутри-папки` в любой папке хранилища. Для этого нужно нажать по названию папки в файловом менеджере `Obsidian` левой кнопкой мыши вместе с нажатым `ctrl` (эта кнопка может быть изменена в настройках плагина), также можно нажать на название папки средней кнопкой мыши, или выбрать соответствующий пункт меню правой кнопки мыши, нажатой по названию папки.

![](<../!!files/AidenLx's Folder Note_create.png>)

Созданная в результате `заметка-внутри-папки` имеет формат `.md`, и название, которое совпадает с названием содержащей эту заметку папки. Визуально папка, в которой уже создана `заметка-внутри-папки`, выделяется в дереве файлов подчеркиванием её названия

![](<../!!files/AidenLx's Folder Note_Folder with note.png>)

При этом сам файл заметки скрыт в `Obsidian` и не отображается внутри папки (может быть изменено в настройках плагина). Однако заметка видна при создании ссылок и в окне открытия заметок (`Ctrl + O`).

Созданная `заметка-внутри-папки` открывается по нажатию левой кнопки мыши по названию папки, в которой она содержится.

В данную `заметку-внутри-папки` может быть внесена любая информация, касающаяся папки и находящихся внутри неё файлов, также плагин в своих настройках позволяет применить шаблоны, поддерживающие переменные (имя папки, путь).

Удаление `заметки-внутри-папки` производится через меню правой кнопки мыши, вызванное по названию папки.

![](<../!!files/AidenLx's Folder Note_Delete.png>)

 > [!attention] ВНИМАНИЕ
> 1. Некоторые другие плагины могут блокировать сочетания клавиш для создания `заметки-внутри-папки`, в этом случае используйте меню правой кнопки мыши.
> 2. В настройках плагина `AidenLx's Folder Note`, в окне заданного шаблона заметки (`Folder Note Template`) можно использовать переменные плагина [Templater](<./Templater.md>), такие как `tp.date.now` и другие для внесения информации в `заметку-внутри-папки`.

> [!bug] Требует проверки?!
> `Заметка-внутри-папки` не взаимодействует как минимум с [Templater](<./Templater.md>), а также *(потенциально, требует проверки)* и с другими плагинами, которые позволяют автоматически применять к создаваемым файлам шаблоны в момент создания файла.
