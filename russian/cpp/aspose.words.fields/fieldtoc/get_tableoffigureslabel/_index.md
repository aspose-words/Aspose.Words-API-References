---
title: "Метод Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel"
linktitle: "get_TableOfFiguresLabel"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel. Получает или задает имя идентификатора последовательности, используемого при построении списка иллюстраций в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.fields/fieldtoc/get_tableoffigureslabel/
---
## FieldToc::get_TableOfFiguresLabel method


Получает или задает имя идентификатора последовательности, используемого при построении списка иллюстраций.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel()
```


## Примеры



Показывает, как заполнить поле TOC записями, используя поля SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поле TOC может создавать запись в своей таблице содержимого для каждого найденного в документе поля SEQ.
// Каждая запись содержит абзац, включающий поле SEQ, и номер страницы, на которой появляется поле.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Поля SEQ отображают счётчик, который увеличивается на каждом поле SEQ.
// Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности.
// идентифицировано свойством "SequenceIdentifier" поля SEQ.
// Используйте свойство "TableOfFiguresLabel", чтобы задать основную последовательность для оглавления.
// Теперь это оглавление будет создавать записи только из полей SEQ, у которых свойство "SequenceIdentifier" установлено в "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Мы можем задать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
// Поля SEQ из этой префиксной последовательности не будут создавать записи в оглавлении.
// Каждая запись оглавления, созданная из поля SEQ основной последовательности, теперь также будет отображать счётчик, который
// префиксная последовательность находится на текущем значении в основном поле SEQ, которое создало запись.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Каждая запись оглавления будет отображать счётчик префиксной последовательности сразу слева
// от номера страницы, на которой находится поле SEQ основной последовательности.
// Мы можем указать пользовательский разделитель, который будет отображаться между этими двумя числами.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Существует два способа использования полей SEQ для заполнения этого оглавления.
// 1 - Вставка поля SEQ, принадлежащего префиксной последовательности оглавления:
// Это поле увеличит счётчик последовательности SEQ для "PrefixSequence" на 1.
// Поскольку это поле не принадлежит основной последовательности, идентифицированной
// свойством "TableOfFiguresLabel" оглавления, оно не будет отображаться как запись.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 - Вставка поля SEQ, принадлежащего основной последовательности оглавления:
// Это поле SEQ создаст запись в оглавлении.
// Запись оглавления будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно расположено.
// Эта запись также будет отображать счётчик, на котором сейчас находится префиксная последовательность,
// отделённый от номера страницы значением свойства SeqenceSeparator оглавления.
// Счётчик "PrefixSequence" равен 1, это поле SEQ основной последовательности находится на странице 2,
// а разделитель — ">", поэтому запись будет отображать "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Вставьте страницу, увеличьте префиксную последовательность на 2 и затем вставьте поле SEQ, чтобы создать запись в оглавлении.
// Префиксная последовательность теперь равна 2, а поле SEQ основной последовательности находится на странице 3,
// поэтому запись оглавления будет отображать "2>3" в своём номере страницы.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## См. также

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
