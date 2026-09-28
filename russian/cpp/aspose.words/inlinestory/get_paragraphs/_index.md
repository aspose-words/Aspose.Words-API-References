---
title: "Aspose::Words::InlineStory::get_Paragraphs method"
linktitle: "get_Paragraphs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::InlineStory::get_Paragraphs method. Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/inlinestory/get_paragraphs/
---
## InlineStory::get_Paragraphs method


Возвращает коллекцию абзацев, которые являются непосредственными дочерними элементами истории.

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::InlineStory::get_Paragraphs() override
```


## Примеры



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


Показывает, как добавить комментарий к абзацу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// В Microsoft Word мы можем щёлкнуть правой кнопкой мыши этот комментарий в теле документа, чтобы отредактировать его или ответить на него.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## См. также

* Class [ParagraphCollection](../../paragraphcollection/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
