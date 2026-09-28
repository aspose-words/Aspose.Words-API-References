---
title: "Метод Aspose::Words::Notes::FootnoteOptions::get_StartNumber"
linktitle: "get_StartNumber"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Notes::FootnoteOptions::get_StartNumber. Указывает начальный номер или символ для первой автоматически нумеруемой сноски в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.notes/footnoteoptions/get_startnumber/
---
## FootnoteOptions::get_StartNumber method


Указывает начальный номер или символ для первой автоматически нумерованной сноски.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_StartNumber() override
```

## Примечания


Это свойство действует только когда [RestartRule](../get_restartrule/) установлен в значение [Continuous](../../footnotenumberingrule/).

## Примеры



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

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
