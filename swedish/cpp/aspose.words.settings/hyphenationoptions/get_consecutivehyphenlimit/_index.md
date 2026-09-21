---
title: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit metod"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit metod. Hämtar eller anger det maximala antalet på varandra följande rader som kan avslutas med bindestreck. Standardvärdet för denna egenskap är 0 i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


Hämtar eller anger det maximala antalet på varandra följande rader som kan avslutas med bindestreck. Standardvärdet för denna egenskap är 0.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## Anmärkningar


Om värdet för denna egenskap sätts till 0 kan ett godtyckligt antal på varandra följande rader avslutas med bindestreck.

Egenskapen har ingen effekt när du sparar till fasta sidformat, t.ex. PDF.

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
