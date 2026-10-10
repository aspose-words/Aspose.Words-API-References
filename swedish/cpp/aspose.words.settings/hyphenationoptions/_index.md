---
title: "Aspose::Words::Settings::HyphenationOptions klass"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::HyphenationOptions klass. Tillåter att konfigurera dokumentets avstavningsalternativ. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


Tillåter att konfigurera dokumentets avstavningsalternativ. För att läsa mer, besök dokumentationsartikeln [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class HyphenationOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | Hämtar eller anger värdet som bestämmer om automatisk avstavning är påslagen för dokumentet. Standardvärdet för denna egenskap är **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | Hämtar eller anger det maximala antalet på varandra följande rader som kan avslutas med bindestreck. Standardvärdet för denna egenskap är 0. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | Hämtar eller anger värdet som bestämmer om ord skrivna med enbart versaler avstavas. Standardvärdet för denna egenskap är **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | Hämtar eller anger avståndet i 1/20 av en punkt från högermarginalen inom vilket du inte vill avstava ord. Standardvärdet för denna egenskap är 360 (0,25 tum). |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | Inställare för [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | Inställare för [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | Inställare för [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | Inställare för [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
