---
title: "Aspose::Words::Notes::Footnote::get_ReferenceMark метод"
linktitle: "get_ReferenceMark"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::Footnote::get_ReferenceMark метод. Получает/устанавливает пользовательскую метку ссылки, используемую для этой сноски. Значение по умолчанию — **empty string**, что означает использование автоматически нумеруемых сносок в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.notes/footnote/get_referencemark/
---
## Footnote::get_ReferenceMark method


Получает/устанавливает пользовательский ссылочный знак, используемый для этой сноски. Значение по умолчанию — **empty string**, что означает использование автонумерованных сносок.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ReferenceMark() const
```

## Примечания


Если это свойство установлено в **empty string** или **null**, то свойство [IsAuto](../get_isauto/) будет автоматически установлено в **true**; если установить в любое другое значение, то [IsAuto](../get_isauto/) будет установлено в **false**.

Формат RTF может хранить только 1 символ в качестве пользовательской метки ссылки, поэтому при экспорте будет записан только первый символ, остальные будут отброшены.

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

## См. также

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
