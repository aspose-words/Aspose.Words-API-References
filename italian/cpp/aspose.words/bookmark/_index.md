---
title: "Aspose::Words::Bookmark classe"
linktitle: "Bookmark"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Bookmark classe. Rappresenta un singolo segnalibro. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/bookmark/
---
## Bookmark class


Rappresenta un singolo segnalibro. Per saperne di più, visita l'articolo di documentazione [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class Bookmark : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Ottiene il nodo che rappresenta la fine del segnalibro. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Ottiene il nodo che rappresenta l'inizio del segnalibro. |
| [get_FirstColumn](./get_firstcolumn/)() | Ottiene l'indice basato su zero della prima colonna dell'intervallo di colonne della tabella associato al segnalibro. |
| [get_IsColumn](./get_iscolumn/)() | Restituisce **true** se questo segnalibro è un segnalibro di colonna di tabella. |
| [get_LastColumn](./get_lastcolumn/)() | Ottiene l'indice basato su zero dell'ultima colonna dell'intervallo di colonne della tabella associato al segnalibro. |
| [get_Name](./get_name/)() | Ottiene o imposta il nome del segnalibro. |
| [get_Text](./get_text/)() | Ottiene il testo racchiuso nel segnalibro. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Rimuove il segnalibro dal documento. Non rimuove il testo all'interno del segnalibro. |
| [set_Name](./set_name/)(const System::String\&) | Setter per [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Imposta il testo racchiuso nel segnalibro. |
| static [Type](./type/)() |  |
## Note


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
