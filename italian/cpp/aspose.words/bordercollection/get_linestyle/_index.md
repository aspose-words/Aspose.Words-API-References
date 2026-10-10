---
title: "Metodo Aspose::Words::BorderCollection::get_LineStyle"
linktitle: "get_LineStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::BorderCollection::get_LineStyle. Ottiene o imposta lo stile del bordo in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/bordercollection/get_linestyle/
---
## BorderCollection::get_LineStyle method


Ottiene o imposta lo stile del bordo.

```cpp
Aspose::Words::LineStyle Aspose::Words::BorderCollection::get_LineStyle()
```

## Note


Restituisce lo stile del primo bordo nella collezione.

Imposta lo stile di tutti i bordi nella collezione escludendo i bordi diagonali.

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

* Enum [LineStyle](../../linestyle/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
