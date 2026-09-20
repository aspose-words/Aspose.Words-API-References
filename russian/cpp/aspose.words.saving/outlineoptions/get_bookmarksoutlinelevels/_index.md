---
title: "Метод Aspose::Words::Saving::OutlineOptions::get_BookmarksOutlineLevels"
linktitle: "get_BookmarksOutlineLevels"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::OutlineOptions::get_BookmarksOutlineLevels. Позволяет задавать уровень структуры для отдельных закладок в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/outlineoptions/get_bookmarksoutlinelevels/
---
## OutlineOptions::get_BookmarksOutlineLevels method


Позволяет задать уровень контура отдельной закладки.

```cpp
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> Aspose::Words::Saving::OutlineOptions::get_BookmarksOutlineLevels() const
```

## Примечания


Если уровень закладки не указан в этой коллекции, используется значение [DefaultBookmarksOutlineLevel](../get_defaultbookmarksoutlinelevel/).

## Примеры



Показывает, как установить уровни контура для закладок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте закладку, внутри которой вложена другая закладка.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// Вставьте другую закладку.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// При сохранении в .pdf закладки можно открыть через выпадающее меню и использовать в качестве якорей большинством читалок.
// Закладки также могут иметь числовые значения уровней структуры,
// что позволяет записям более низкого уровня скрывать дочерние записи более высокого уровня при сворачивании в просмотрщике.
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// Мы можем удалить два элемента, чтобы осталась только обозначение уровня структуры для "Bookmark 1".
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// Существует девять уровней структуры. Их нумерация будет оптимизирована во время операции сохранения.
// В этом случае уровни "5" и "9" станут "2" и "3".
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Очистка этой коллекции сохранит закладки и разместит их все на одном уровне структуры.
outlineLevels->Clear();
```

## См. также

* Class [BookmarksOutlineLevelCollection](../../bookmarksoutlinelevelcollection/)
* Class [OutlineOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
