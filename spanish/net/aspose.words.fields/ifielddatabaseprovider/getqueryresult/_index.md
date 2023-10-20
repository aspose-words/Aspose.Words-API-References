---
title: IFieldDatabaseProvider.GetQueryResult
linktitle: GetQueryResult
articleTitle: GetQueryResult
second_title: Aspose.Words para .NET
description: IFieldDatabaseProvider GetQueryResult método. Devuelve el resultado de la consulta en C#.
type: docs
weight: 10
url: /es/net/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider.GetQueryResult method

Devuelve el resultado de la consulta.

```csharp
public FieldDatabaseDataTable GetQueryResult(string fileName, string connection, string query, 
    FieldDatabase field)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | La ruta completa y el nombre de archivo de la base de datos especificada en el modificador de campo \d. |
| connection | String | La conexión a los datos especificados en el campo \c cambia. |
| query | String | El conjunto de instrucciones SQL que consultan la base de datos especificada en el campo \s. |
| field | FieldDatabase | El campo que se está actualizando. |

### Valor_devuelto

El[`FieldDatabaseDataTable`](../../fielddatabasedatatable/) instancia que debe usarse para la actualización del campo.

### Ver también

* class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* class [FieldDatabase](../../fielddatabase/)
* interface [IFieldDatabaseProvider](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
