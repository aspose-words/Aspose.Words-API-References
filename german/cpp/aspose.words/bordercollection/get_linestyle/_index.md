---
title: "Aspose::Words::BorderCollection::get_LineStyle Methode"
linktitle: "get_LineStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::get_LineStyle Methode. Gibt den Rahmenstil zurück oder legt ihn in C++ fest."
type: docs
weight: 10000
url: /de/cpp/aspose.words/bordercollection/get_linestyle/
---
## BorderCollection::get_LineStyle method


Liefert oder setzt den Rahmenstil.

```cpp
Aspose::Words::LineStyle Aspose::Words::BorderCollection::get_LineStyle()
```

## Hinweise


Gibt den Stil des ersten Rahmens in der Sammlung zurück.

Legt den Stil aller Rahmen in der Sammlung fest, ausgenommen diagonale Rahmen.

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

* Enum [LineStyle](../../linestyle/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
