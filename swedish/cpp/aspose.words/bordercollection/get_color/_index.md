---
title: "Aspose::Words::BorderCollection::get_Color‑metod"
linktitle: "get_Color"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BorderCollection::get_Color‑metod. Hämtar eller anger kantens färg i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/bordercollection/get_color/
---
## BorderCollection::get_Color method


Hämtar eller anger kantens färg.

```cpp
System::Drawing::Color Aspose::Words::BorderCollection::get_Color()
```

## Anmärkningar


Returnerar färgen på den första kanten i samlingen.

Anger färgen på alla kanter i samlingen, exklusive diagonala kanter.

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
