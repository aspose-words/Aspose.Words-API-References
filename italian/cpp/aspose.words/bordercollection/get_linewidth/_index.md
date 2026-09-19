---
title: "Aspose::Words::BorderCollection::get_LineWidth metodo"
linktitle: "get_LineWidth"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BorderCollection::get_LineWidth metodo. Ottiene o imposta la larghezza del bordo in punti in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/bordercollection/get_linewidth/
---
## BorderCollection::get_LineWidth method


Ottiene o imposta la larghezza del bordo in punti.

```cpp
double Aspose::Words::BorderCollection::get_LineWidth()
```

## Note


Restituisce la larghezza del primo bordo nella collezione.

Imposta la larghezza di tutti i bordi nella collezione, esclusi i bordi diagonali.

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
