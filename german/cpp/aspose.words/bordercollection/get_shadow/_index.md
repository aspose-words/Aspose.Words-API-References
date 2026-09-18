---
title: "Aspose::Words::BorderCollection::get_Shadow Methode"
linktitle: "get_Shadow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::get_Shadow Methode. Gibt einen Wert zurück oder legt ihn fest, der angibt, ob der Rahmen in C++ einen Schatten hat."
type: docs
weight: 13000
url: /de/cpp/aspose.words/bordercollection/get_shadow/
---
## BorderCollection::get_Shadow method


Liefert oder setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat.

```cpp
bool Aspose::Words::BorderCollection::get_Shadow()
```

## Hinweise


Gibt den Wert des ersten Rahmens in der Sammlung zurück.

Legt den Wert für alle Rahmen in der Sammlung fest, ausgenommen diagonale Rahmen.

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
