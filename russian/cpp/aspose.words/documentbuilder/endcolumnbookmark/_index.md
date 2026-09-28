---
title: "Aspose::Words::DocumentBuilder::EndColumnBookmark method"
linktitle: "EndColumnBookmark"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::EndColumnBookmark метод. Отмечает текущую позицию в документе как конец закладки столбца. Позиция должна находиться в ячейке таблицы в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder::EndColumnBookmark method


Помечает текущую позицию в документе как конец закладки столбца. Позиция должна находиться в ячейке таблицы.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndColumnBookmark(const System::String &bookmarkName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | const System::String\& | Имя закладки. |

### ReturnValue

Узел конца закладки, который только что был создан.
## Примечания


Столбцовая закладка охватывает один или несколько столбцов в диапазоне строк. Чтобы создать корректную закладку, необходимо вызвать как [StartColumnBookmark()](../), так и [EndColumnBookmark()](../) с одинаковым параметром *bookmarkName*.

Некорректно сформированные закладки или закладки с дублирующимися именами будут игнорироваться при сохранении документа.

Фактическая позиция вставленного узла [BookmarkEnd](../../bookmarkend/) может отличаться от текущей позиции построителя документа.

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

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
