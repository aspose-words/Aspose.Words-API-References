---
title: "Metodo Aspose::Words::Bookmark::get_Name"
linktitle: "get_Name"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Bookmark::get_Name. Ottiene o imposta il nome del segnalibro in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


Ottiene o imposta il nome del segnalibro.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Esempi



Mostra come inserire un segnalibro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un segnalibro valido ha un nome, un nodo BookmarkStart e un nodo BookmarkEnd.
// Qualsiasi spazio nei nomi dei segnalibri verrà convertito in underscore se apriamo il documento salvato con Microsoft Word.
// Se evidenziamo il nome del segnalibro in Microsoft Word tramite Inserisci -> Collegamenti -> Segnalibro, e premiamo "Vai a",
// il cursore salterà al testo compreso tra i nodi BookmarkStart e BookmarkEnd.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// I segnalibri sono memorizzati in questa raccolta.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## Vedi anche

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
