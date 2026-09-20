---
title: "Перечисление Aspose::Words::Notes::EndnotePosition"
linktitle: "EndnotePosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Notes::EndnotePosition. Определяет положение сноски в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.notes/endnoteposition/
---
## EndnotePosition enum


Определяет положение сноски.

```cpp
enum class EndnotePosition
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| EndOfSection | 0 | Сноски выводятся в конце раздела. |
| EndOfDocument | 3 | Сноски выводятся в конце документа. |


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

## См. также

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
