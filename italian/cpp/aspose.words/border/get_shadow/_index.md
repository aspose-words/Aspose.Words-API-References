---
title: "Metodo Aspose::Words::Border::get_Shadow"
linktitle: "get_Shadow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Border::get_Shadow. Ottiene o imposta un valore che indica se il bordo ha un'ombra in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


Ottiene o imposta un valore che indica se il bordo ha un'ombra.

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## Note


In Microsoft Word, affinché un bordo abbia un'ombra, i bordi su tutti e quattro i lati (sinistra, superiore, destra e inferiore) devono essere dello stesso tipo, larghezza, colore e tutti devono avere la proprietà Shadow impostata su **true**.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
