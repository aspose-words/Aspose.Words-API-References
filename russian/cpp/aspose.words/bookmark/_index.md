---
title: "Aspose::Words::Bookmark класс"
linktitle: "Закладка"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Bookmark класс. Представляет одну закладку. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/bookmark/
---
## Bookmark class


Представляет одну закладку. Чтобы узнать больше, посетите статью документации [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class Bookmark : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Получает узел, представляющий конец закладки. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Получает узел, представляющий начало закладки. |
| [get_FirstColumn](./get_firstcolumn/)() | Получает нулевой индекс первой колонки диапазона столбцов таблицы, связанного с закладкой. |
| [get_IsColumn](./get_iscolumn/)() | Возвращает **true**, если эта закладка является закладкой столбца таблицы. |
| [get_LastColumn](./get_lastcolumn/)() | Получает нулевой индекс последней колонки диапазона столбцов таблицы, связанного с закладкой. |
| [get_Name](./get_name/)() | Получает или задает имя закладки. |
| [get_Text](./get_text/)() | Получает текст, заключённый в закладку. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Удаляет закладку из документа. Не удаляет текст внутри закладки. |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Задаёт текст, заключённый в закладку. |
| static [Type](./type/)() |  |
## Примечания


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
