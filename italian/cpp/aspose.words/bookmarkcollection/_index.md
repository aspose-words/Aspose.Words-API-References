---
title: "Aspose::Words::BookmarkCollection class"
linktitle: "BookmarkCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BookmarkCollection class. Una collezione di oggetti Bookmark che rappresentano i segnalibri nell'intervallo specificato. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


Una collezione di oggetti [Bookmark](../bookmark/) che rappresentano i segnalibri nell'intervallo specificato. Per saperne di più, visita l'articolo di documentazione [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clear](./clear/)() | Rimuove tutti i segnalibri da questa collezione e dal documento. |
| [get_Count](./get_count/)() | Restituisce il numero di segnalibri nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce un segnalibro all'indice specificato. |
| [idx_get](./idx_get/)(const System::String\&) | Restituisce un segnalibro per nome. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Rimuove il segnalibro specificato dal documento. |
| [Remove](./remove/)(const System::String\&) | Rimuove un segnalibro con il nome specificato. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un segnalibro all'indice specificato. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
