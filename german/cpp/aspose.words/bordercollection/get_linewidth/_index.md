---
title: "Aspose::Words::BorderCollection::get_LineWidth Methode"
linktitle: "get_LineWidth"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::get_LineWidth Methode. Gibt die Rahmenbreite in Punkten zurück oder legt sie in C++ fest."
type: docs
weight: 11000
url: /de/cpp/aspose.words/bordercollection/get_linewidth/
---
## BorderCollection::get_LineWidth method


Liefert oder setzt die Rahmenbreite in Punkten.

```cpp
double Aspose::Words::BorderCollection::get_LineWidth()
```

## Hinweise


Gibt die Breite des ersten Rahmens in der Sammlung zurück.

Legt die Breite aller Rahmen in der Sammlung fest, ausgenommen diagonale Rahmen.

## Beispiele



Zeigt, wie man einen grünen, welligen Seitenrahmen mit Schatten erstellt.
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

## Siehe auch

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
