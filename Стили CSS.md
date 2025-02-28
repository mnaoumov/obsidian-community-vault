---
title: Стили CSS
---

# Стили CSS

## Установка пользовательских CSS

1. Открываем папку `путь/к/хранилищу/.obsidian/snippets` и создаём там сниппет, например, `long-file-name.css`.
2. Открываем в настройках `Obsidian` и активируем новосозданный сниппет. Если его не видно, возможно сначала нужно нажать кнопку `Обновить`. ![](<./!!files/install-css.png>)

## clean-embeds.css

сниппет который убирает заголовок, полосу, кнопку ссылки и отступ у встраиваемых заметок, чтобы в режиме просмотра они выглядели как просто текст без признаков что он из другой заметки

> [!NOTE]- clean-embeds.css
>
> ```css
> /*
>     clean-embeds-all.css snippet
> 
>     Removes title, link, padding, margins from embeds,
>     so they really look like the same note.
> 
>     This will not require a `cssclass` to be set but work for _all_ notes.
>     Derived from the `clean-embeds.css` snippet.
> 
>     2021-08-24 Matthias C. Hormann (Moonbase59)
> 
>     TODO: Find out how to correct PDF export. L/R margins & vspace too large on embeds.
> */
> 
> /* remove title and the table from the "Metatable" plugin */
> .markdown-preview-view .markdown-embed-title,
> .markdown-preview-view .obsidian-metatable {
>   display: none;
> }
> 
> /*
>   For links to embeds NOT to be shown, uncomment the following
>   and comment out the other section below.
> */
> 
> /*
> .markdown-preview-view .markdown-embed-link,
> .markdown-preview-view .file-embed-link {
>   display: none;
> }
> */
> 
> /*
>   For links to embeds to BE shown, uncomment the following
>   until the "End link show/hide stuff" comment
>   and comment out the section above.
> */
> 
> /* Link icon */
> .markdown-preview-view .markdown-embed-link,
> .markdown-preview-view .file-embed-link {
>   top: 0;
>   right: 0;
>   left: unset;
>   text-align: right;
>   border: none;
>   margin: 0;
>   width: 24px;
>   height: 24px;
>   color: var(--text-faint);
>   cursor: pointer;
> }
> 
> /* for Ars Magna theme and others that change ::before */
> .markdown-preview-view .markdown-embed-link::before,
> .markdown-preview-view .file-embed-link::before {
>   display: none;
> }
> 
> /* Link icon size & hide */
> .markdown-preview-view .file-embed-link svg,
> .markdown-preview-view .markdown-embed-link svg {
>   height: 24px;
>   width: 24px;
>   opacity: 0;
>   display: unset;
> }
> 
> /* show on hover */
> .markdown-preview-view .markdown-embed:hover .file-embed-link svg,
> .markdown-preview-view .markdown-embed:hover .markdown-embed-link svg {
>   opacity: 1;
> }
> 
> /* change background on hover, to exactly see what’s embedded */
> .markdown-preview-view .markdown-embed:hover,
> .markdown-preview-view .file-embed:hover {
>   background-color: var(--background-secondary) !important;
> }
> 
> /* End link show/hide stuff */
> 
> 
> 
> /* remove border and scroll */
> /* unfortunately needs !important for some themes */
> .markdown-preview-view .markdown-embed,
> .markdown-preview-view .file-embed {
>   border: none !important;
>   padding: 0 !important;
>   margin: 0 !important;
> }
> 
> .markdown-preview-view .markdown-embed-content,
> .markdown-preview-view .markdown-embed-content > .markdown-preview-view { 
>   max-height: unset;
>   padding: 0 !important; /* !important for "Pisum" theme */
>   margin: 0;
>   border: 0;
> }
> 
> /* remove <br> between internal embeds */
> .markdown-preview-section div > br {
>   display: none;
> }
> 
> 
>  /*remove vertical space added by markdown-preview-sizer 
>  это я изменил↓*/
>  /*div.markdown-preview-sizer.markdown-preview-section {
>   min-height: unset !important;
>   padding-bottom: 0 !important;
> }*/
> /* special considerations for printing (PDF export) */
> @media print {
> 
>   /* remove frontmatter box if "Show frontmatter" was enabled */
>   /* Also remove metadata table from "Metatable" plugin */
>   pre.frontmatter,
>   .obsidian-metatable {
>     display: none;
>   }
> }
> ```

## long-file-name.css

Для того чтобы вместо

![](<./!!files/long-file-name-1.png>)

отображалось

![](<./!!files/long-file-name-2.png>)

> [!NOTE]- long-file-name.css
>
> ```css
> .nav-file-title-content,
> .nav-folder-title-content {
>     white-space: break-spaces;
> }
> ```

## editor-line-width.css

Используйте для изменения ширины текста в режиме редактора.

Было

![](<./!!files/editor-line-width-1.png>)

Станет

![](<./!!files/editor-line-width-2.png>)

Для задания ширины строки укажите в свойствах заметки, в `cssclasses` нужную ширину в пикселях в формате `widthXXXX`, где `XXXX` числа из ряда `500`, `800`, `1000`, `1200`. Стандартная ширина строки в режиме редактора - `700` пикселей, поэтому при значении `500` ширина строки даже уменьшается.

При желании можно добавить новые строки или изменить файл `.css` прописав в выделенных местах своё значение ширины строки.

![](<./!!files/editor-line-width-3.png>)

> [!NOTE]- editor-line-width.css
>
> ```css
> .width500 {
>    --file-line-width: 500px;
>}
>
>.width800 {
>    --file-line-width: 800px;
>}
>
>.width1000 {
>    --file-line-width: 1000px;
>}
>
>.width1200 {
>    --file-line-width: 1200px;
>}
> ```
