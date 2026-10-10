---
title: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult‑metod"
linktitle: "GetQueryResult"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult‑metod. Returnerar frågeresultat i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


Returnerar frågeresultat.

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | System::String | Den fullständiga sökvägen och filnamnet för databasen som anges i \d‑fältväxeln. |
| anslutning | System::String | Anslutningen till data som anges i \c‑fältväxeln. |
| fråga | System::String | Mängden SQL‑instruktioner som frågar databasen som anges i \s‑fältväxeln. |
| fält | System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\> | Fältet som uppdateras. |

### ReturnValue

Den [FieldDatabaseDataTable](../../fielddatabasedatatable/)‑instans som ska användas för fältets uppdatering.

## Se även

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
