---
title: "Aspose::Words::PageSetup::get_LinesPerPage metodo"
linktitle: "get_LinesPerPage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_LinesPerPage metodo. Ottiene o imposta il numero di righe per pagina nella griglia del documento in C++."
type: docs
weight: 26000
url: /it/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


Ottiene o imposta il numero di righe per pagina nella griglia del documento.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## Note


Il valore minimo della proprietà è 1. Il valore massimo dipende dall'altezza della pagina e dalla dimensione del carattere dello stile Normale. L'interlinea minima è il 136 percento della dimensione del carattere. Ad esempio, il numero massimo di righe per pagina di una pagina Letter con margini di un pollice è 39.

Per impostazione predefinita, la proprietà ha un valore in cui l'interlinea è 1,5 volte maggiore della dimensione del carattere dello stile Normale.

## Esempi



Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Abilita il pitching e poi usalo per impostare il numero di righe per pagina in questa sezione.
// Una dimensione del carattere sufficientemente grande sposterà alcune righe nella pagina successiva per evitare la sovrapposizione dei caratteri.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
