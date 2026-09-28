---
title: "Метод Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier"
linktitle: "get_SequenceIdentifier"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier. Получает или задает имя, присвоенное серии элементов, которые должны быть пронумерованы, в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.fields/fieldseq/get_sequenceidentifier/
---
## FieldSeq::get_SequenceIdentifier method


Получает или задаёт имя, присвоенное серии элементов, которые должны быть пронумерованы.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier()
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


Показывает создание нумерации с использованием полей SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поля SEQ отображают счётчик, который увеличивается на каждом поле SEQ.
// Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности.
// идентифицировано свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, которое будет отображать текущее значение счётчика "MySequence",
// после использования свойства "ResetNumber" для установки его в 100.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Отобразите следующее число в этой последовательности с помощью другого поля SEQ.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Вставьте заголовок уровня 1.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Вставьте ещё одно поле SEQ из той же последовательности и настройте его сбрасывать счётчик до 1 при каждом заголовке.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// Указанный выше заголовок — заголовок уровня 1, поэтому счётчик для этой последовательности сбрасывается до 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Перейдите к следующему числу этой последовательности.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```

## См. также

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
