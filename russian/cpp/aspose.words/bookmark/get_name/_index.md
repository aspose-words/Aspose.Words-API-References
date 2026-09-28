---
title: "Метод Aspose::Words::Bookmark::get_Name"
linktitle: "get_Name"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Bookmark::get_Name. Получает или задает имя закладки в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


Получает или задает имя закладки.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Примеры



Показывает, как вставить закладку.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Корректная закладка имеет имя, узел BookmarkStart и узел BookmarkEnd.
// Любые пробелы в именах закладок будут заменены на подчеркивания, если открыть сохранённый документ в Microsoft Word.
// Если выделить имя закладки в Microsoft Word через Вставка -> Ссылки -> Закладка и нажать «Перейти»,
// курсор переместится к тексту, заключённому между узлами BookmarkStart и BookmarkEnd.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// Закладки хранятся в этой коллекции.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## См. также

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
