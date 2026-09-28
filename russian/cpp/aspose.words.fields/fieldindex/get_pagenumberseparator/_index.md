---
title: "Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator метод"
linktitle: "get_PageNumberSeparator"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator метод. Получает или задает последовательность символов, используемую для разделения записи индекса и её номера страницы в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.fields/fieldindex/get_pagenumberseparator/
---
## FieldIndex::get_PageNumberSeparator method


Получает или задает последовательность символов, используемую для разделения записи указателя и её номера страницы.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator()
```


## Примеры



Показывает, как изменить разделитель номеров страниц в поле INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// а номер страницы, содержащей поле XE, — справа.
// Запись INDEX будет группировать поля XE с совпадающими значениями в свойстве "Text".
// в одну запись, а не создавать отдельную запись для каждого поля XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Если наше поле INDEX содержит запись для группы полей XE,
// эта запись будет отображать номер каждой страницы, содержащей поле XE, принадлежащее этой группе.
// Мы можем задать пользовательские разделители, чтобы настроить отображение этих номеров страниц.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageNumberListSeparator(u" & ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\l \" & \"", index->GetFieldCode());
ASSERT_TRUE(index->get_HasPageNumberSeparator());

// После вставки этих полей XE поле INDEX отобразит "First entry, on page(s) 2 & 3 & 4".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

ASSERT_EQ(u" XE  \"First entry\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageNumberList.docx");
```

## См. также

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
