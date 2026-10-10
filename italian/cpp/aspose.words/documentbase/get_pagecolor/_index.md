---
title: "Metodo Aspose::Words::DocumentBase::get_PageColor"
linktitle: "get_PageColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBase::get_PageColor. Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione più semplice di BackgroundShape in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione più semplice di [BackgroundShape](../get_backgroundshape/).

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## Note


Questa proprietà offre un modo semplice per specificare un colore di pagina solido per il documento. Impostare questa proprietà crea e imposta una [BackgroundShape](../get_backgroundshape/) appropriata.

Se il colore della pagina non è impostato (ad esempio non esiste una forma di sfondo nel documento) restituisce **Empty**.

## Esempi



Mostra come impostare il colore di sfondo per tutte le pagine di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## Vedi anche

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
