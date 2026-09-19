---
title: "Metodo Aspose::Words::BorderCollection::get_DistanceFromText"
linktitle: "get_DistanceFromText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::BorderCollection::get_DistanceFromText. Ottiene o imposta la distanza del bordo dal testo in punti in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


Ottiene o imposta la distanza del bordo dal testo in punti.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## Note


Ottiene la distanza dal testo per il primo bordo.

Imposta la distanza dal testo per tutti i bordi nella collezione, esclusi i bordi diagonali.

Non ha alcun effetto e verrà automaticamente riportato a zero per i bordi delle celle della tabella.

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
