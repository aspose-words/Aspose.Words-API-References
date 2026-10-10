---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps metod"
linktitle: "get_HyphenateCaps"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps metod. Hämtar eller anger värdet som bestämmer om ord skrivna med enbart stora bokstäver ska bindestrecksdelas. Standardvärdet för denna egenskap är true i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.settings/hyphenationoptions/get_hyphenatecaps/
---
## HyphenationOptions::get_HyphenateCaps method


Hämtar eller anger värdet som bestämmer om ord skrivna med enbart versaler avstavas. Standardvärdet för denna egenskap är **true**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps() const
```


## Exempel



Visar hur man konfigurerar automatisk avstavning.
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

## Se även

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
