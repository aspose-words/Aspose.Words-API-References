---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone метод"
linktitle: "get_HyphenationZone"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone метод. Получает или задает расстояние в 1/20 пункта от правого поля, в пределах которого не следует переносить слова. Значение по умолчанию для этого свойства равно 360 (0,25 дюйма) в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


Получает или задает расстояние в 1/20 пункта от правого поля, в пределах которого не следует переносить слова. Значение по умолчанию для этого свойства равно 360 (0,25 дюйма).

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
```


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

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
