---
title: "Aspose::Words::BorderCollection::get_LineStyle metod"
linktitle: "get_LineStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BorderCollection::get_LineStyle metod. Hämtar eller anger kantstilen i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/bordercollection/get_linestyle/
---
## BorderCollection::get_LineStyle method


Hämtar eller anger kantstilen.

```cpp
Aspose::Words::LineStyle Aspose::Words::BorderCollection::get_LineStyle()
```

## Anmärkningar


Returnerar stilen på den första kanten i samlingen.

Anger stilen på alla kanter i samlingen, exklusive diagonala kanter.

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

* Enum [LineStyle](../../linestyle/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
