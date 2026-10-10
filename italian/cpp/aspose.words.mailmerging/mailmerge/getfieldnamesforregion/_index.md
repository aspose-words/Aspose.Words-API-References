---
title: "Metodo Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion"
linktitle: "GetFieldNamesForRegion"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion. Restituisce una raccolta di nomi di campi di mail merge disponibili nella regione in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


Restituisce una raccolta di nomi di campi di mail merge disponibili nella regione.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| regionName | const System::String\& | Nome della regione (non sensibile a maiuscole/minuscole). |
## Note


Restituisce i nomi completi dei campi di merge includendo il prefisso opzionale. Non elimina i nomi di campo duplicati.

Se il documento contiene più regioni con lo stesso nome, viene elaborata la prima regione.

Un nuovo array di stringhe viene creato ad ogni chiamata.

## Vedi anche

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


Restituisce una raccolta di nomi di campi di mail merge disponibili nella regione.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| regionName | const System::String\& | Nome della regione (non sensibile a maiuscole/minuscole). |
| regionIndex | int32_t | Indice della regione (basato su zero). |
## Note


Restituisce i nomi completi dei campi di merge includendo il prefisso opzionale. Non elimina i nomi di campo duplicati.

Se il documento contiene più regioni con lo stesso nome, viene elaborata la N‑esima regione (basata su zero).

Un nuovo array di stringhe viene creato ad ogni chiamata.

## Vedi anche

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
