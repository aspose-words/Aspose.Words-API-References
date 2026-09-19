---
title: "Metodo Aspose::Words::ParagraphFormat::get_SnapToGrid"
linktitle: "get_SnapToGrid"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ParagraphFormat::get_SnapToGrid. Specifica se il paragrafo corrente deve utilizzare le impostazioni delle linee della griglia del documento per pagina durante il layout del contenuto nel paragrafo in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


Specifica se il paragrafo corrente deve utilizzare le impostazioni delle linee della griglia del documento per pagina durante il layout del contenuto nel paragrafo.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
