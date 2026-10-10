---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone metod"
linktitle: "get_HyphenationZone"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone metod. Hämtar eller anger avståndet i 1/20 av en punkt från högermarginalen inom vilket du inte vill dela ord med bindestreck. Standardvärdet för denna egenskap är 360 (0,25 tum) i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


Hämtar eller anger avståndet i 1/20 av en punkt från högermarginalen inom vilket du inte vill avstava ord. Standardvärdet för denna egenskap är 360 (0,25 tum).

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
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
