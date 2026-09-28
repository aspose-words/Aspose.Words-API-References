---
title: "Aspose::Words::Notes::FootnoteNumberingRule enum"
linktitle: "FootnoteNumberingRule"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::FootnoteNumberingRule enum. Определяет, когда автоматическая нумерация сносок или конечных сносок перезапускается в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enum


Определяет, когда автоматическая нумерация сносок или концевых сносок перезапускается.

```cpp
enum class FootnoteNumberingRule
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Continuous | 0 | Нумерация непрерывна по всему документу. |
| RestartSection | 1 | Нумерация перезапускается в каждом разделе. |
| RestartPage | 2 | Нумерация перезапускается на каждой странице. Действительно только для сносок. |
| Default | n/a | Равно [Continuous](./). |


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
