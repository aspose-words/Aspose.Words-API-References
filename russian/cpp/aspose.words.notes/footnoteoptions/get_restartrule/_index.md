---
title: "Метод Aspose::Words::Notes::FootnoteOptions::get_RestartRule"
linktitle: "get_RestartRule"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Notes::FootnoteOptions::get_RestartRule. Определяет, когда автоматическая нумерация перезапускается в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.notes/footnoteoptions/get_restartrule/
---
## FootnoteOptions::get_RestartRule method


Определяет, когда автоматическая нумерация перезапускается.

```cpp
Aspose::Words::Notes::FootnoteNumberingRule Aspose::Words::Notes::FootnoteOptions::get_RestartRule() override
```


## Примеры



Показывает, как перезапустить нумерацию сносок/конечных сносок в определённых местах документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Сноски и концевые сноски — это способ прикрепить ссылку или побочный комментарий к тексту
// которая не мешает потоку основного текста.
// Вставка сноски/концевой сноски добавляет небольшой верхний индекс в виде символа ссылки
// в основном тексте, где мы вставляем сноску/концевую сноску.
// Каждая сноска/концевая сноска также создает запись, состоящую из символа, соответствующего ссылке
// символ в основном тексте. Текст ссылки, который мы передаем методу "InsertEndnote" построителя документа.
// Записи сносок по умолчанию отображаются внизу каждой страницы, содержащей
// их символы ссылок, а концевые сноски отображаются в конце документа.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// По умолчанию символ ссылки для каждой сноски и концевой сноски — её индекс
// среди всех сносок/концевых сносок документа. Каждый документ поддерживает отдельные подсчёты
// для сносок и конечных сносок и не перезапускает эти подсчёты ни в каком месте.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// Мы можем использовать свойство "RestartRule", чтобы заставить документ перезапустить
// нумерацию сносок/конечных сносок на новой странице или в разделе.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```

## См. также

* Enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
