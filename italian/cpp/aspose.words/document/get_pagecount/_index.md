---
title: "Aspose::Words::Document::get_PageCount metodo"
linktitle: "get_PageCount"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_PageCount metodo. Ottiene il numero di pagine del documento calcolato dall'operazione di layout della pagina più recente in C++."
type: docs
weight: 43000
url: /it/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


Ottiene il numero di pagine del documento calcolato dall'ultima operazione di layout della pagina.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## Esempi



Mostra come contare il numero di pagine nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Verifica il conteggio delle pagine previsto del documento.
ASSERT_EQ(3, doc->get_PageCount());

// L'ottenimento della proprietà PageCount ha invocato il layout della pagina del documento per calcolare il valore.
// Questa operazione non dovrà essere ripetuta durante il rendering del documento in un formato di salvataggio a pagina fissa,
// come .pdf. Così puoi risparmiare tempo, specialmente con documenti più complessi.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
