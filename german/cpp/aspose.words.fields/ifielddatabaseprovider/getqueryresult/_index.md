---
title: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult Methode"
linktitle: "GetQueryResult"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult Methode. Gibt das Abfrageergebnis in C++ zurück."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


Gibt das Abfrageergebnis zurück.

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | System::String | Der vollständige Pfad und Dateiname der in dem \d-Feldschalter angegebenen Datenbank. |
| Verbindung | System::String | Die Verbindung zu den Daten, die im \c-Feldschalter angegeben sind. |
| Abfrage | System::String | Der Satz von SQL-Anweisungen, die die in dem \s-Feldschalter angegebene Datenbank abfragen. |
| field | System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\> | Das zu aktualisierende Feld. |

### ReturnValue

Die [FieldDatabaseDataTable](../../fielddatabasedatatable/) Instanz, die für die Aktualisierung des Feldes verwendet werden sollte.

## Siehe auch

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
