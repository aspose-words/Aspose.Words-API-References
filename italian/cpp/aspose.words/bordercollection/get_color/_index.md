---
title: "Aspose::Words::BorderCollection::get_Color metodo"
linktitle: "get_Color"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BorderCollection::get_Color metodo. Ottiene o imposta il colore del bordo in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/bordercollection/get_color/
---
## BorderCollection::get_Color method


Ottiene o imposta il colore del bordo.

```cpp
System::Drawing::Color Aspose::Words::BorderCollection::get_Color()
```

## Note


Restituisce il colore del primo bordo nella collezione.

Imposta il colore di tutti i bordi nella collezione, esclusi i bordi diagonali.

## Esempi



Mostra come creare un bordo di pagina verde ondulato con un'ombra.
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

## Vedi anche

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
