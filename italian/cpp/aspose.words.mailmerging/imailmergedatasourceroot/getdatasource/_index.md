---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource metodo"
linktitle: "GetDataSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource metodo. Il motore di unione della posta di Aspose.Words invoca questo metodo quando incontra l'inizio di una regione di unione della posta di livello superiore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


Il motore di unione di posta Aspose.Words invoca questo metodo quando incontra l'inizio di una regione di unione di posta di livello superiore.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableName | System::String | Il nome della regione di stampa unione come specificato nel documento modello. Non sensibile alle maiuscole. |

### ReturnValue

Un oggetto fonte dati che fornirà l'accesso ai record dei dati della tabella specificata.
## Note


Quando i motori di unione della posta di Aspose.Words popolano un documento con i dati e incontrano MERGEFIELD TableStart:TableName, invocano [GetDataSource()](./) su questo oggetto. La tua implementazione deve restituire un nuovo oggetto origine dati. Aspose.Words utilizzerà l'origine dati restituita per popolare la regione di unione della posta.

Se un'origine dati (tabella) con il nome specificato non esiste, la tua implementazione dovrebbe restituire **null**.

## Vedi anche

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
