---
title: "Метод Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine. Получает или задает, помещать ли подзаписи в одну строку с основной записью в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


Получает или задает, следует ли размещать подпункты в той же строке, что и основной пункт.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## Примеры



Показывает, как работать с подзаписями в поле INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// а номер страницы, содержащей поле XE, — справа.
// Запись INDEX будет собирать все поля XE с совпадающими значениями в свойстве "Text"
// в одну запись, а не создавать отдельную запись для каждого поля XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// Поля XE, имеющие свойство Text, значение которого становится заголовком записи INDEX.
// Если это значение содержит два строковых сегмента, разделённых двоеточием (поле INDEX будет рассматривать :) как разделитель,
// первый сегмент является заголовком, а второй сегмент станет подзаголовком.
// Поле INDEX сначала группирует записи в алфавитном порядке, затем, если существует несколько полей XE с одинаковыми
// заголовками, поле INDEX дополнительно подгруппирует их по значениям этих заголовков.
// Может быть несколько уровней подгруппировки, в зависимости от того, сколько раз
// свойства Text полей XE сегментируются таким образом.
// По умолчанию группа записей поля INDEX создаёт новую строку для каждого подзаголовка в этой группе.
// Мы можем установить флаг RunSubentriesOnSameLine в true, чтобы сохранить заголовок,
// и каждый подзаголовок группы в одну строку, что сделает поле INDEX более компактным.
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// Вставьте два поля XE, каждое на новой странице, с одинаковым заголовком под названием "Heading 1",
// которые поле INDEX будет использовать для их группировки.
// Если RunSubentriesOnSameLine установлен в false, то таблица INDEX создаст три строки:
// одна строка для группирующего заголовка "Heading 1" и ещё по одной строке для каждого подзаголовка.
// Если RunSubentriesOnSameLine установлен в true, то таблица INDEX создаст одну строку
// запись, охватывающую заголовок и каждый подзаголовок.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 1");

ASSERT_EQ(u" XE  \"Heading 1:Subheading 1\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 2");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + System::String::Format(u"Field.INDEX.XE.Subheading.docx"));
```

## См. также

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
