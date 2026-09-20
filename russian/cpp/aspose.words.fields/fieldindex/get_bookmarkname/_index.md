---
title: "Aspose::Words::Fields::FieldIndex::get_BookmarkName метод"
linktitle: "Метод Aspose::Words::Fields::FieldAsk::set_DefaultResponse"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldIndex::get_BookmarkName метод. Получает или задает имя закладки, отмечающей часть документа, используемую для построения указателя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldindex/get_bookmarkname/
---
## FieldIndex::get_BookmarkName method


Получает или задает имя закладки, отмечающей часть документа, используемую для построения указателя.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_BookmarkName()
```


## Примеры



Показывает, как создать поле INDEX и затем использовать поля XE для заполнения его записями.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева
// и страницу, содержащую поле XE, справа.
// Если у полей XE одинаковое значение в их свойстве "Text",
// поле INDEX сгруппирует их в одну запись.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Настройте поле INDEX так, чтобы оно отображало только поля XE, находящиеся в пределах
// закладки с именем "MainBookmark" и у которых свойство "EntryType" имеет значение "A".
// Для полей INDEX и XE свойство "EntryType" использует только первый символ строкового значения.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// На новой странице начните закладку с именем, соответствующим значению
// свойства "BookmarkName" поля INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// Поле INDEX подхватит эту запись, потому что она находится внутри закладки,
// и её тип записи также соответствует типу записи поля INDEX.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Вставьте поле XE, которое не появится в INDEX, потому что типы записей не совпадают.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Закончите закладку и вставьте поле XE после неё.
// Оно того же типа, что и поле INDEX, но не появится
// поскольку находится за пределами границ закладки.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```

## См. также

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
