---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop metodo"
linktitle: "get_LinesToDrop"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop metodo. Ottiene o imposta il numero di righe del testo del paragrafo usate per calcolare l'altezza del capolettera in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


Ottiene o imposta il numero di righe del testo del paragrafo usate per calcolare l'altezza del drop cap.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## Esempi



Mostra come impostare la dimensione di un capolettera.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifica la proprietà "LinesToDrop" per designare un paragrafo come capolettera,
// che lo trasformerà in una grande lettera maiuscola che decorerà il paragrafo successivo.
// Assegna a questa proprietà il valore 4 per dare al capolettera l'altezza di quattro righe di testo.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// Reimposta la proprietà "LinesToDrop" a 0 per trasformare il paragrafo successivo in un paragrafo ordinario.
// Il testo in questo paragrafo avvolgerà il capolettera.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
