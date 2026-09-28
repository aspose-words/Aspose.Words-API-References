---
title: "Aspose::Words::Settings::HyphenationOptions class"
linktitle: "HyphenationOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::HyphenationOptions class. Позволяет настроить параметры переноса слов в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


Позволяет настраивать параметры переноса слов в документе. Чтобы узнать больше, посетите статью документации [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class HyphenationOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | Получает или задает значение, определяющее, включено ли автоматическое перенесение слов в документе. Значение по умолчанию для этого свойства — **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | Получает или задает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства равно 0. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | Получает или задает значение, определяющее, будут ли переноситься слова, написанные заглавными буквами. Значение по умолчанию для этого свойства — **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | Получает или задает расстояние в 1/20 пункта от правого поля, в пределах которого не следует переносить слова. Значение по умолчанию для этого свойства равно 360 (0,25 дюйма). |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | Сеттер для [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | Сеттер для [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | Сеттер для [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | Сеттер для [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как настроить автоматический перенос.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
