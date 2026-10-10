---
title: "Aspose::Words::Border::get_Shadow-Methode"
linktitle: "get_Shadow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::get_Shadow-Methode. Liest oder setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat, in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


Liefert oder setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat.

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## Hinweise


In Microsoft Word muss ein Rahmen, um einen Schatten zu haben, dass die Rahmen auf allen vier Seiten (links, oben, rechts und unten) vom selben Typ, derselben Breite, derselben Farbe sind und alle die Shadow‑Eigenschaft auf **true** gesetzt haben.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
