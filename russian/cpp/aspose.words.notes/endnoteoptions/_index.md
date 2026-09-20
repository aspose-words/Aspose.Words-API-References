---
title: "Класс Aspose::Words::Notes::EndnoteOptions"
linktitle: "EndnoteOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Notes::EndnoteOptions. Представляет параметры нумерации концевых сносок для документа или раздела. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.notes/endnoteoptions/
---
## EndnoteOptions class


Представляет параметры нумерации концевых сносок для документа или раздела. Чтобы узнать больше, посетите статью документации [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/).

```cpp
class EndnoteOptions : public Aspose::Words::Notes::IFootnoteOptions
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_NumberStyle](./get_numberstyle/)() override | Указывает формат номера для автоматически нумерованных концевых сносок. |
| [get_Position](./get_position/)() | Указывает положение сносок. |
| [get_RestartRule](./get_restartrule/)() override | Определяет, когда автоматическая нумерация перезапускается. |
| [get_StartNumber](./get_startnumber/)() override | Указывает начальный номер или символ для первой автоматически нумеруемой сноски. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) override | Сеттер для [Aspose::Words::Notes::EndnoteOptions::get_NumberStyle](./get_numberstyle/). |
| [set_Position](./set_position/)(Aspose::Words::Notes::EndnotePosition) | Сеттер для [Aspose::Words::Notes::EndnoteOptions::get_Position](./get_position/). |
| [set_RestartRule](./set_restartrule/)(Aspose::Words::Notes::FootnoteNumberingRule) override | Сеттер для [Aspose::Words::Notes::EndnoteOptions::get_RestartRule](./get_restartrule/). |
| [set_StartNumber](./set_startnumber/)(int32_t) override | Сеттер для [Aspose::Words::Notes::EndnoteOptions::get_StartNumber](./get_startnumber/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как выбрать другое место, где документ собирает и отображает свои сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Сноска — это способ добавить ссылку или боковой комментарий к тексту
// которая не мешает потоку основного текста.
// Вставка сноски добавляет небольшой надстрочный символ ссылки
// в основном тексте, где мы вставляем сноску.
// Каждая сноска также создает запись в конце документа, состоящую из символа
// который соответствует символу ссылки в основном тексте.
// Текст ссылки, который мы передаем методу "InsertEndnote" построителя документа.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// Мы можем использовать свойство "Position", чтобы определить, где документ разместит все свои сноски.
// Если мы установим значение свойства "Position" в "EndnotePosition.EndOfDocument",
// каждая сноска появится в коллекции в конце документа. Это значение по умолчанию.
// Если мы установим значение свойства "Position" в "EndnotePosition.EndOfSection",
// каждая сноска появится в коллекции в конце раздела, текст которого содержит маркер ссылки сноски.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```


Показывает, как изменить стиль нумерации символов ссылок сноски/концевой сноски.
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
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// По умолчанию символ ссылки для каждой сноски и концевой сноски — её индекс
// среди всех сносок/концевых сносок документа. Каждый документ поддерживает отдельные подсчёты
// для сносок и для концевых сносок. По умолчанию сноски отображают свои номера арабскими цифрами,
// а концевые сноски отображают свои номера строчными римскими цифрами.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// Мы можем использовать свойство "NumberStyle", чтобы применить пользовательские стили нумерации к сноскам и концевым сноскам.
// Это не повлияет на сноски/концевые сноски с пользовательскими символами ссылок.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```


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


Показывает, как задать номер, с которого документ начинает нумерацию сносок/конечных сносок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Сноски и концевые сноски — это способ прикрепить ссылку или побочный комментарий к тексту
// которая не мешает потоку основного текста.
// Вставка сноски/концевой сноски добавляет небольшой верхний индекс в виде символа ссылки
// в основном тексте, где мы вставляем сноску/концевую сноску.
// Каждая сноска/конечная сноска также создаёт запись, состоящую из символа
// который соответствует символу ссылки в основном тексте.
// Текст ссылки, который мы передаем методу "InsertEndnote" построителя документа.
// Записи сносок по умолчанию отображаются внизу каждой страницы, содержащей
// их символы ссылок, а концевые сноски отображаются в конце документа.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// По умолчанию символ ссылки для каждой сноски и концевой сноски — её индекс
// среди всех сносок/концевых сносок документа. Каждый документ поддерживает отдельные подсчёты
// для сносок и для конечных сносок, которые обе начинаются с 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// Мы можем использовать свойство "StartNumber", чтобы заставить документ
// начать нумерацию сноски или конечной сноски с другого числа.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## См. также

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
