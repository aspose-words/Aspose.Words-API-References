---
title: "Aspose::Words::Notes::FootnotePosition enum"
linktitle: "FootnotePosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::FootnotePosition enum. Определяет положение сноски в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.notes/footnoteposition/
---
## FootnotePosition enum


Определяет положение сноски.

```cpp
enum class FootnotePosition
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| BottomOfPage | 1 | Сноски выводятся внизу каждой страницы. |
| BeneathText | 2 | Сноски выводятся под текстом на каждой странице. |


## Примеры



Показывает, как выбрать другое место, где документ собирает и отображает свои сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Сноска — это способ прикрепить ссылку или побочный комментарий к тексту
// которая не мешает потоку основного текста.
// Вставка сноски добавляет небольшой верхний индекс в виде символа ссылки
// в основном тексте, где мы вставляем сноску.
// Каждая сноска также создает запись внизу страницы, состоящую из символа
// который соответствует символу ссылки в основном тексте.
// Текст ссылки, который мы передаем методу "InsertFootnote" построителя документа.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// Мы можем использовать свойство "Position", чтобы определить, где документ разместит все свои сноски.
// Если мы установим значение свойства "Position" в "FootnotePosition.BottomOfPage",
// каждая сноска будет отображаться внизу страницы, содержащей её маркер ссылки. Это значение по умолчанию.
// Если мы установим значение свойства "Position" в "FootnotePosition.BeneathText",
// каждая сноска будет отображаться в конце текста страницы, содержащего её маркер ссылки.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```

## См. также

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
