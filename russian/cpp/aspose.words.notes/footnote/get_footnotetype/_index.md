---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType метод"
linktitle: "get_FootnoteType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType метод. Возвращает значение, указывающее, является ли это сноской или концевой сноской в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


Возвращает значение, указывающее, является ли это сноской или концевой сноской.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## Примеры



Показывает разницу между сносками и концевыми сносками.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два способа прикрепления нумерованных ссылок к тексту. Оба этих ссылки добавят
// маленькую надстрочную метку ссылки в месте, где мы их вставляем.
// Метка ссылки по умолчанию — это порядковый номер ссылки среди всех ссылок в документе.
// Каждая ссылка также создаст запись, которая будет иметь ту же метку ссылки, что и в основном тексте
// и текст ссылки, который мы передадим методу "InsertFootnote" построителя документа.
// 1 -  Сноска, запись которой появится на той же странице, что и текст, к которому она относится:
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  Конечная сноска, запись которой будет отображаться в конце документа:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## См. также

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
