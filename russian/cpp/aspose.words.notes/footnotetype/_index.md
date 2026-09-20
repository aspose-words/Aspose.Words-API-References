---
title: "Aspose::Words::Notes::FootnoteType enum"
linktitle: "FootnoteType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::FootnoteType enum. Указывает, является ли это сноской или концевой сноской в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


Указывает, является ли это сноской или концевой сноской.

```cpp
enum class FootnoteType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Footnote | 0 | Объект является сноской. |
| Концевая сноска | 1 | Объект является концевой сноской. |

## Примечания


И сноски, и концевые сноски представлены объектами класса [Footnote](./). Используйте [FootnoteType](../footnote/get_footnotetype/) для различения сносок и концевых сносок.

## Примеры



Показывает, как ссылаться на текст с помощью сноски и концевой сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте некоторый текст и пометьте его сноской, у которой свойство IsAuto по умолчанию установлено в "true",
// чтобы маркер, видимый в основном тексте, был автоматически пронумерован как "1",
// и сноска появится внизу страницы.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Вставьте ещё текст и пометьте его концевой сноской с пользовательским маркером ссылки,
// который будет использоваться вместо числа "2" и установит "IsAuto" в false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Сноски всегда появляются внизу текста, к которому они относятся,
// поэтому разрыв страницы не повлияет на сноску.
// С другой стороны, концевые сноски всегда находятся в конце документа
// поэтому этот разрыв страницы перенесёт концевую сноску на следующую страницу.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


Показывает, как вставлять и настраивать сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте текст и сослаться на него с помощью сноски. Эта сноска разместит небольшую надстрочную ссылку
// после текста, на который она ссылается, и создаст запись под основным текстом внизу страницы.
// Эта запись будет содержать маркер ссылки сноски и текст ссылки,
// которые мы передадим методу "InsertFootnote" построителя документа.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Если это свойство установлено в "true", то маркер ссылки нашей сноски
// будет её индексом среди всех сносок раздела.
// Это первая сноска, поэтому её маркер будет "1".
ASSERT_TRUE(footnote->get_IsAuto());

// Мы можем переместить построитель документа внутрь сноски, чтобы отредактировать её текст ссылки.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Мы можем задать пользовательский маркер ссылки, который сноска будет использовать вместо своего порядкового номера.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Закладка с флагом "IsAuto", установленным в true, всё равно покажет свой реальный индекс
// даже если предыдущие закладки отображают пользовательские маркеры, поэтому маркер этой закладки будет "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## См. также

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
