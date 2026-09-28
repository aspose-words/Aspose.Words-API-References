---
title: "Aspose::Words::Fields::FieldIndex::get_SequenceSeparator метод"
linktitle: "get_SequenceSeparator"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldIndex::get_SequenceSeparator метод. Получает или задает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.fields/fieldindex/get_sequenceseparator/
---
## FieldIndex::get_SequenceSeparator method


Получает или задает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_SequenceSeparator()
```


## Примеры



Показывает, как разделить документ на части, комбинируя поля INDEX и SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// а номер страницы, содержащей поле XE, — справа.
// Если у полей XE одинаковое значение в их свойстве "Text",
// поле INDEX сгруппирует их в одну запись.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// В свойстве SequenceName укажите последовательность поля SEQ. Каждая запись этого поля INDEX теперь также будет отображать
// номер, на котором находится счётчик последовательности, в месте поля XE, которое создало эту запись.
index->set_SequenceName(u"MySequence");

// Установите текст, который будет окружать номера последовательности и страниц, чтобы объяснить их значение пользователю.
// Запись, созданная с этой конфигурацией, будет отображать что-то вроде \"MySequence at 1 on page 1\" рядом с номером страницы.
// PageNumberSeparator и SequenceSeparator не могут быть длиннее 15 символов.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// Поля SEQ отображают счётчик, который увеличивается на каждом поле SEQ.
// Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности.
// идентифицировано свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, которое перемещает последовательность \"MySequence\" к 1.
// Это поле не отличается от обычного текста документа. Оно не будет отображаться в оглавлении поля INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// Вставьте поле XE, которое создаст запись в поле INDEX.
// Поскольку \"MySequence\" находится на 1, а это поле XE — на странице 2, вместе с пользовательскими разделителями, которые мы определили выше,
// Эта запись INDEX этого поля будет отображать "Cat" слева и "MySequence at 1 on page 2" справа.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// Вставьте разрыв страницы и используйте поля SEQ, чтобы продвинуть "MySequence" до 3.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// Вставьте поле XE с тем же свойством Text, что и выше.
// Запись INDEX будет группировать поля XE с совпадающими значениями в свойстве "Text".
// в одну запись, а не создавать отдельную запись для каждого поля XE.
// Поскольку мы на странице 2 с "MySequence" равным 3, ", 3 on page 3" будет добавлен к той же записи INDEX, что выше.
// Часть с номером страницы этой записи INDEX теперь будет отображать "MySequence at 1 on page 2, 3 on page 3".
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// Вставьте поле XE с новым и уникальным значением свойства Text.
// Это добавит новую запись, с MySequence равным 3 на странице 4.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## См. также

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
