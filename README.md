LaTeX-проект для диссертации и презентации к защите.

## Особенности
* Кодировка: UTF-8.
* Стандарт оформления: ГОСТ Р 7.0.11-2011.
* Поддерживаемые движки: pdfTeX, XeTeX, LuaTeX.
* Поддерживаемые реализации библиографии: встроенная на движке BibTeX, BibLaTeX
на движке Biber.
* В проекте оставлены только материалы, относящиеся к диссертации и презентации.

## Сборка
Основные команды:

* `make dissertation` — сборка диссертации.
* `make presentation` — сборка презентации.
* `make` — сборка диссертации и презентации.
* `make clean` — очистка временных файлов.
* `make distclean` — полная очистка временных файлов.

При необходимости можно запускать сборку напрямую через `latexmk`, но основной
предполагаемый сценарий работы в этом проекте — через `Makefile`.

## Структура
* [dissertation.tex](dissertation.tex): главный файл диссертации.
* **[папка Dissertation](Dissertation/):** структурированная система файлов с
  содержимым диссертации.
  * **папка images:** изображения, относящиеся только к диссертации.
  * [setup.tex](Dissertation/setup.tex): упрощённые настройки оформления
    диссертации.
  * [introduction.tex](Dissertation/introduction.tex): введение.
  * [part1.tex](Dissertation/part1.tex), [part2.tex](Dissertation/part2.tex),
    [part3.tex](Dissertation/part3.tex): основные главы.
  * [conclusion.tex](Dissertation/conclusion.tex): заключение.
  * [references.tex](Dissertation/references.tex): список литературы.
  * [appendix.tex](Dissertation/appendix.tex): приложения.
* [presentation.tex](presentation.tex): главный файл презентации.
* **[папка Presentation](Presentation/):** структурированная система файлов с
  презентацией.
  * **папка images:** изображения, относящиеся только к презентации.
  * [setup.tex](Presentation/setup.tex): настройки оформления презентации.
  * [preamble.tex](Presentation/preamble.tex): начальные слайды.
  * [content.tex](Presentation/content.tex): основное содержимое презентации.
  * [conclusion.tex](Presentation/conclusion.tex): завершающие слайды.
  * [appendix.tex](Presentation/appendix.tex): запасные слайды.
* **[папка Documents](Documents/):** полезные документы и материалы по оформлению.
* **[папка PSCyr](PSCyr/):** пакет PSCyr и сопутствующие инструкции.
* **[папка BibTeX-Styles](BibTeX-Styles/):** подборка русских стилевых пакетов
  BibTeX под UTF-8.
* **[папка common](common/):** общие файлы настроек и данных проекта.
  * [data.tex](common/data.tex): основные сведения о работе.
  * [packages.tex](common/packages.tex): общие пакеты.
  * [styles.tex](common/styles.tex): общие стили оформления.
  * [setup.tex](common/setup.tex): общие настройки проекта и выбор библиографии.
  * [fonts.tex](common/fonts.tex): настройки шрифтов.
  * [renames.tex](common/renames.tex): переопределение стандартных подписей и названий.
* **[папка biblio](biblio/):** файлы с библиографией.
  * [author.bib](biblio/author.bib): публикации автора по теме работы.
  * [registered.bib](biblio/registered.bib): зарегистрированные патенты и программы.
  * [external.bib](biblio/external.bib): внешние источники.
* **папка images:** общие изображения проекта.
* **папка listings:** дополнительные файлы листингов и сопутствующих материалов.

## Дополнительные файлы
* [Makefile](Makefile), [compress.mk](compress.mk), [unix.mk](unix.mk),
  [windows.mk](windows.mk), [latexmkrc](latexmkrc): файлы системы сборки.
* [usercfg.mk](usercfg.mk): пользовательские настройки сборки.
* [indent.yaml](indent.yaml): настройки форматирования исходного кода для
  [latexindent](https://www.ctan.org/pkg/latexindent).
* [.editorconfig](.editorconfig): настройки текстовых редакторов, поддерживающих
  стандарт [editorconfig](https://editorconfig.org/).
* [siunitx.cfg](siunitx.cfg): определения величин SI для библиотеки
  [siunitx](https://ctan.org/pkg/siunitx).
* [tikz.tex](tikz.tex): файл изолированной сборки векторной графики
  [tikz](https://www.ctan.org/pkg/pgf).

## Что удалено из исходного шаблона
Из проекта намеренно убраны части шаблона, которые не используются в текущей
работе:

* автореферат и все связанные с ним файлы;
* материалы для печатных booklet-версий;
* handout-версия презентации;
* шаблонные файлы рассылки и генерации конвертов;
* шаблонная документация, GitHub-обвязка и вспомогательные шаблонные артефакты.

## Основа проекта
Проект основан на шаблоне *Russian-Phd-LaTeX-Dissertation-Template* и адаптирован
под текущую магистерскую работу с сохранением только нужной структуры.
