---
title: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult metodo"
linktitle: "GetQueryResult"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult metodo. Restituisce il risultato della query in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


Restituisce il risultato della query.

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | System::String | Il percorso completo e il nome file del database specificato nello switch del campo \d. |
| connection | System::String | La connessione ai dati specificata nello switch del campo \c. |
| query | System::String | Il set di istruzioni SQL che interrogano il database specificato nell'opzione di campo \s. |
| campo | System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\> | Il campo in fase di aggiornamento. |

### ReturnValue

L'istanza [FieldDatabaseDataTable](../../fielddatabasedatatable/) che dovrebbe essere usata per l'aggiornamento del campo.

## Vedi anche

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
