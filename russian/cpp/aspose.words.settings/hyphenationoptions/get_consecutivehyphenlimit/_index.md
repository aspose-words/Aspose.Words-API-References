---
title: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit метод"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit метод. Получает или задает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства равно 0 в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


Получает или задает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства равно 0.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## Примечания


Если значение этого свойства установлено в 0, любое количество последовательных строк может заканчиваться дефисами.

Это свойство не оказывает влияния при сохранении в форматы фиксированных страниц, например PDF.

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
