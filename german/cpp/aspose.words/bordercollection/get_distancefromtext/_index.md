---
title: "Aspose::Words::BorderCollection::get_DistanceFromText-Methode"
linktitle: "get_DistanceFromText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::get_DistanceFromText-Methode. Ruft den Abstand des Rahmens vom Text in Punkten ab oder legt ihn fest in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


Liefert oder setzt den Abstand des Rahmens vom Text in Punkten.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## Hinweise


Ermittelt den Abstand vom Text für den ersten Rahmen.

Legt den Abstand vom Text für alle Rahmen in der Sammlung fest, ausgenommen diagonale Rahmen.

Hat keine Wirkung und wird für Rahmen von Tabellenzellen automatisch auf Null zurückgesetzt.

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
