---
title: "Aspose::Words::BorderCollection::get_Shadow metodo"
linktitle: "get_Shadow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BorderCollection::get_Shadow metodo. Ottiene o imposta un valore che indica se il bordo ha un'ombra in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/bordercollection/get_shadow/
---
## BorderCollection::get_Shadow method


Ottiene o imposta un valore che indica se il bordo ha un'ombra.

```cpp
bool Aspose::Words::BorderCollection::get_Shadow()
```

## Note


Ottiene il valore dal primo bordo nella collezione.

Imposta il valore per tutti i bordi nella collezione, esclusi i bordi diagonali.

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
