---
title: "Metodo Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource"
linktitle: "GetChildDataSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource. Il motore di stampa unione di Aspose.Words invoca questo metodo quando incontra l'inizio di una regione di stampa unione annidata in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


Il motore di mail merge di Aspose.Words invoca questo metodo quando incontra l'inizio di una regione di mail merge annidata.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableName | System::String | Il nome della regione di stampa unione come specificato nel documento modello. Non sensibile alle maiuscole. |

### ReturnValue

Un oggetto fonte dati che fornirà l'accesso ai record dei dati della tabella specificata.
## Note


Quando i motori di stampa unione di Aspose.Words popolano una regione di stampa unione con i dati e incontrano l'inizio di una regione di stampa unione annidata nella forma MERGEFIELD TableStart:TableName, invocano [GetChildDataSource()](./) sull'oggetto fonte dati corrente. La tua implementazione deve restituire un nuovo oggetto fonte dati che fornirà l'accesso ai record figli del record genitore corrente. Aspose.Words utilizzerà la fonte dati restituita per popolare la regione di stampa unione annidata.

Di seguito sono riportate le regole che l'implementazione di [GetChildDataSource()](./) deve rispettare.

Se la tabella rappresentata da questo oggetto fonte dati ha una tabella figlia (di dettaglio) correlata con il nome specificato, la tua implementazione deve restituire un nuovo oggetto [IMailMergeDataSource](../) che fornirà l'accesso ai record figli del record corrente. Un esempio di ciò è la relazione Ordini / DettagliOrdine. Supponiamo che l'oggetto [IMailMergeDataSource](../) corrente rappresenti la tabella Ordini e che abbia un record d'ordine corrente. Successivamente, Aspose.Words incontra "MERGEFIELD TableStart:OrderDetails" nel documento e invoca [GetChildDataSource()](./). Devi creare e restituire un oggetto [IMailMergeDataSource](../) che consentirà ad Aspose.Words di accedere al record DettagliOrdine per l'ordine corrente.

Se questo oggetto fonte dati non ha una relazione con la tabella dal nome specificato, devi restituire un oggetto [IMailMergeDataSource](../) che fornirà l'accesso a tutti i record della tabella specificata.

Se una tabella con il nome specificato non esiste, la tua implementazione dovrebbe restituire **null**.

## Vedi anche

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
