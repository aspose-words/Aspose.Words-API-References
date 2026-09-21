---
title: "Aspose::Words::BorderCollection::get_Shadow‑metod"
linktitle: "get_Shadow"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BorderCollection::get_Shadow‑metod. Hämtar eller anger ett värde som visar om kanten har en skugga i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/bordercollection/get_shadow/
---
## BorderCollection::get_Shadow method


Hämtar eller anger ett värde som indikerar om kanten har en skugga.

```cpp
bool Aspose::Words::BorderCollection::get_Shadow()
```

## Anmärkningar


Hämtar värdet från den första kanten i samlingen.

Anger värdet för alla kanter i samlingen, exklusive diagonala kanter.

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
