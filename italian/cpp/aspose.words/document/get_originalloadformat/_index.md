---
title: "Metodo Aspose::Words::Document::get_OriginalLoadFormat"
linktitle: "get_OriginalLoadFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_OriginalLoadFormat metodo. Ottiene il formato del documento originale che è stato caricato in questo oggetto in C++."
type: docs
weight: 41000
url: /it/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


Ottiene il formato del documento originale che è stato caricato in questo oggetto.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## Note


Se hai creato un nuovo documento vuoto, restituisce il valore [Doc](../../loadformat/).

## Esempi



Mostra come recuperare i dettagli dell'operazione di caricamento di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## Vedi anche

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
