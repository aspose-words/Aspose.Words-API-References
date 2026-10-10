---
title: "Aspose::Words::BorderCollection::get_Color-Methode"
linktitle: "get_Color"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::get_Color-Methode. Ruft die Rahmenfarbe ab oder legt sie fest in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/bordercollection/get_color/
---
## BorderCollection::get_Color method


Liefert oder setzt die Rahmenfarbe.

```cpp
System::Drawing::Color Aspose::Words::BorderCollection::get_Color()
```

## Hinweise


Gibt die Farbe des ersten Rahmens in der Sammlung zurück.

Legt die Farbe aller Rahmen in der Sammlung fest, ausgenommen diagonale Rahmen.

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
