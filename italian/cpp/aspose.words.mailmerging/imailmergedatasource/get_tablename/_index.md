---
title: "Metodo Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName"
linktitle: "get_TableName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName. Restituisce il nome della fonte dati in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.mailmerging/imailmergedatasource/get_tablename/
---
## IMailMergeDataSource::get_TableName method


Restituisce il nome della fonte dati.

```cpp
virtual System::String Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName()=0
```


### ReturnValue

Il nome della fonte dati. Stringa vuota se la fonte dati non ha un nome.
## Note


Se stai implementando [IMailMergeDataSource](../), restituisci il nome della fonte dati da questa proprietà.

Aspose.Words utilizza questo nome per confrontarlo con il nome della regione di stampa unione specificato nel documento modello. Il confronto tra il nome della fonte dati e il nome della regione di stampa unione non distingue tra maiuscole e minuscole.

## Vedi anche

* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
