---
title: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult method"
linktitle: "GetQueryResult"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult method. Devuelve el resultado de la consulta en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


Devuelve el resultado de la consulta.

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | System::String | La ruta completa y el nombre de archivo de la base de datos especificada en el interruptor de campo \d. |
| connection | System::String | La conexión a los datos especificada en el interruptor de campo \c. |
| consulta | System::String | El conjunto de instrucciones SQL que consultan la base de datos especificada en el interruptor de campo \s. |
| campo | System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\> | El campo que se está actualizando. |

### ReturnValue

La instancia [FieldDatabaseDataTable](../../fielddatabasedatatable/) que debe usarse para la actualización del campo.

## Ver también

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
