---
title: "Metodo Aspose::Words::BookmarkCollection::idx_get"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::BookmarkCollection::idx_get. Restituisce un segnalibro per nome in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/bookmarkcollection/idx_get/
---
## BookmarkCollection::idx_get(const System::String\&) method


Restituisce un segnalibro per nome.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(const System::String &bookmarkName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nome del segnalibro non sensibile a maiuscole/minuscole. |
## Note


Restituisce **null** se il segnalibro con il nome specificato non può essere trovato.

## Vedi anche

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarkCollection::idx_get(int32_t) method


Restituisce un segnalibro all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella collezione. |
## Note


L'indice parte da zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

## Vedi anche

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
