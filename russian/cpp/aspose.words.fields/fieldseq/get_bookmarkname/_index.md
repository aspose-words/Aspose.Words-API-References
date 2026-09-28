---
title: "Метод Aspose::Words::Fields::FieldSeq::get_BookmarkName"
linktitle: "Метод Aspose::Words::Fields::FieldAsk::set_DefaultResponse"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldSeq::get_BookmarkName. Получает или задает имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем расположении, в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


Получает или задаёт имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем расположении.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## Примеры



Показывает, как комбинировать оглавление и поля последовательности.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поле TOC может создавать запись в своей таблице содержимого для каждого найденного в документе поля SEQ.
// Каждая запись содержит абзац, в котором находится поле SEQ,
// и номер страницы, на которой появляется поле.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Настройте это поле TOC так, чтобы у него было свойство SequenceIdentifier со значением "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Настройте это поле TOC так, чтобы оно выбирало только поля SEQ, находящиеся в пределах закладки
// с именем "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// Поля SEQ отображают счётчик, который увеличивается на каждом поле SEQ.
// Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности.
// идентифицировано свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, у которого идентификатор последовательности совпадает с
// свойством TableOfFiguresLabel у TOC. Это поле не создаст запись в оглавлении, поскольку оно находится за пределами
// границ закладки, обозначенных "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// Последовательность этого поля SEQ совпадает со свойством "TableOfFiguresLabel" у TOC и находится в пределах границ закладки.
// Абзац, содержащий это поле, появится в оглавлении как запись.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// Последовательность этого поля SEQ не совпадает со свойством "TableOfFiguresLabel" у TOC,
// но находится в пределах границ закладки. Его абзац не появится в оглавлении как запись.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// Последовательность этого поля SEQ совпадает со свойством "TableOfFiguresLabel" у TOC и находится в пределах границ закладки.
// Это поле также ссылается на другую закладку. Содержимое этой закладки появится в записи оглавления для этого поля SEQ.
// Само поле SEQ не будет отображать содержимое этой закладки.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Создайте закладку с содержимым, которое появится в записи оглавления из-за того, что вышеуказанное поле SEQ ссылается на неё.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## См. также

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
