---
title: "Aspose::Words::PageSetup::get_CharactersPerLine metodo"
linktitle: "get_CharactersPerLine"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_CharactersPerLine metodo. Ottiene o imposta il numero di caratteri per riga nella griglia del documento in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


Ottiene o imposta il numero di caratteri per riga nella griglia del documento.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## Note


Il valore minimo della proprietà è 1. Il valore massimo dipende dalla larghezza della pagina e dalla dimensione del carattere dello stile Normale. La spaziatura minima dei caratteri è il 90 percento della dimensione del carattere. Per esempio, il numero massimo di caratteri per riga di una pagina Letter con margini di un pollice è 43.

Per impostazione predefinita, la proprietà ha un valore in cui la spaziatura dei caratteri è uguale alla dimensione del carattere dello stile Normale.

## Esempi



Mostra come specificare un valore per il numero di caratteri che ogni riga può contenere.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Abilita il pitching e poi usalo per impostare il numero di caratteri per riga in questa sezione.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// Il numero di caratteri dipende anche dalla dimensione del carattere.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
