---
title: "Metodo Aspose::Words::Document::get_VersionsCount"
linktitle: "get_VersionsCount"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_VersionsCount. Ottiene il numero di versioni del documento che è stato memorizzato nel documento DOC in C++."
type: docs
weight: 57000
url: /it/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


Ottiene il numero di versioni del documento che è stato memorizzato nel documento DOC.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## Note


Le versioni in Microsoft Word sono accessibili tramite il menu File/Versions. Microsoft Word supporta le versioni solo per i file DOC.

Questa proprietà consente di rilevare se nel documento erano presenti versioni salvate prima di aprirlo in Aspose.Words. Aspose.Words non fornisce altro supporto per le versioni dei documenti. Se salvi questo documento usando Aspose.Words, il documento verrà salvato senza versioni.

## Esempi



Mostra come lavorare con la funzionalità di conteggio delle versioni dei documenti Microsoft Word più vecchi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// Possiamo leggere questa proprietà di un documento, ma non possiamo preservarla durante il salvataggio.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
