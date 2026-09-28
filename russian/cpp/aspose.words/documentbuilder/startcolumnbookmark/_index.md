---
title: "Aspose::Words::DocumentBuilder::StartColumnBookmark method"
linktitle: "StartColumnBookmark"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::StartColumnBookmark method. Помечает текущую позицию в документе как начало столбцовой закладки. Позиция должна находиться в ячейке таблицы в C++."
type: docs
weight: 69000
url: /ru/cpp/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder::StartColumnBookmark method


Помечает текущую позицию в документе как начало столбцовой закладки. Позиция должна находиться в ячейке таблицы.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartColumnBookmark(const System::String &bookmarkName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | const System::String\& | Имя закладки. |

### ReturnValue

Узел начала закладки, только что созданный.
## Примечания


Столбцовая закладка охватывает один или несколько столбцов в диапазоне строк. Чтобы создать корректную закладку, необходимо вызвать как [StartColumnBookmark()](../), так и [EndColumnBookmark()](../) с одинаковым параметром *bookmarkName*.

Некорректно сформированные закладки или закладки с дублирующимися именами будут игнорироваться при сохранении документа.

Фактическая позиция вставленного узла [BookmarkStart](../../bookmarkstart/) может отличаться от текущей позиции построителя документа.

## Примеры



Показывает, как создать закладку столбца.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// Ячейки 1,2,4,5 будут отмечены закладкой.
builder->StartColumnBookmark(u"MyBookmark_1");
// Некорректно сформированные закладки или закладки с дублирующимися именами будут игнорироваться при сохранении документа.
builder->StartColumnBookmark(u"MyBookmark_1");
builder->StartColumnBookmark(u"BadStartBookmark");
builder->Write(u"Cell 1");

builder->InsertCell();
builder->Write(u"Cell 2");

builder->InsertCell();
builder->Write(u"Cell 3");

builder->EndRow();

builder->InsertCell();
builder->Write(u"Cell 4");

builder->InsertCell();
builder->Write(u"Cell 5");
builder->EndColumnBookmark(u"MyBookmark_1");
builder->EndColumnBookmark(u"MyBookmark_1");

ASSERT_THROW(static_cast<std::function<void()>>([&builder]() -> void
{
    builder->EndColumnBookmark(u"BadEndBookmark");

builder->InsertCell();
builder->Write(u"Cell 6");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"Bookmarks.CreateColumnBookmark.docx");
```

## См. также

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
