---
title: "Aspose::Words::BorderCollection::get_DistanceFromText‑metod"
linktitle: "get_DistanceFromText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BorderCollection::get_DistanceFromText‑metod. Hämtar eller anger avståndet för kanten från texten i punkter i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


Hämtar eller anger avståndet för kanten från texten i punkter.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## Anmärkningar


Hämtar avståndet från texten för den första kanten.

Anger avståndet från texten för alla kanter i samlingen, exklusive diagonala kanter.

Har ingen effekt och återställs automatiskt till noll för kanter i tabellceller.

## Exempel



Visar hur man skapar en grön vågig sidkantslinje med en skugga.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## Se även

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
