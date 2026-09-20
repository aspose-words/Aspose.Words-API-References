---
title: "Метод Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName"
linktitle: "get_PageRangeBookmarkName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName. Получает или задает имя закладки, обозначающей диапазон страниц, который вставляется как номер страницы записи в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.fields/fieldxe/get_pagerangebookmarkname/
---
## FieldXE::get_PageRangeBookmarkName method


Получает или задает имя закладки, обозначающей диапазон страниц, который вставляется как номер страницы записи.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName()
```


## Примеры



Показывает, как указать охваченные закладкой страницы в виде диапазона страниц для записи поля INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// а номер страницы, содержащей поле XE, — справа.
// Запись INDEX будет собирать все поля XE с совпадающими значениями в свойстве "Text"
// в одну запись, а не создавать отдельную запись для каждого поля XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Для записей INDEX, отображающих диапазоны страниц, можно указать строку-разделитель
// которая будет отображаться между номером первой страницы и номером последней.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// Если поле XE задает закладку с помощью свойства PageRangeBookmarkName,
// его запись INDEX покажет диапазон страниц, охваченных закладкой
// вместо номера страницы, содержащей поле XE.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// Вставьте закладку, начинающуюся на странице 3 и заканчивающуюся на странице 5.
// Запись INDEX для поля XE, ссылающегося на эту закладку, отобразит этот диапазон страниц.
// В нашей таблице запись INDEX будет отображать "My entry, on page(s) 3 to 5".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## См. также

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
