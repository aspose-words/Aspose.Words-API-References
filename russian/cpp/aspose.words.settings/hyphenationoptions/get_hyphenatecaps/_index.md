---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps метод"
linktitle: "get_HyphenateCaps"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps метод. Получает или задает значение, определяющее, будут ли переноситься слова, написанные заглавными буквами. Значение по умолчанию для этого свойства равно true в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.settings/hyphenationoptions/get_hyphenatecaps/
---
## HyphenationOptions::get_HyphenateCaps method


Получает или задает значение, определяющее, будут ли переноситься слова, написанные заглавными буквами. Значение по умолчанию для этого свойства — **true**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps() const
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
