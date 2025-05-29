---
title: IFieldDatabaseProvider.GetQueryResult
linktitle: GetQueryResult
articleTitle: GetQueryResult
second_title: Aspose.Words para .NET
description: Descubra el método GetQueryResult de IFieldDatabaseProvider para una recuperación de datos eficiente. ¡Optimice sus consultas y mejore el rendimiento de su base de datos hoy mismo!
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
| fileName | String | La ruta completa y el nombre del archivo de la base de datos especificada en el campo modificador \d. |
| connection | String | La conexión a los datos especificados en el campo \c. |
| query | String | El conjunto de instrucciones SQL que consultan la base de datos especificada en el campo \s. |
| field | FieldDatabase | El campo que se está actualizando. |

### Valor_devuelto

El[`FieldDatabaseDataTable`](../../fielddatabasedatatable/) instancia que debe utilizarse para la actualización del campo.

## Ejemplos

Muestra cómo extraer datos de una base de datos e insertarlos como un campo en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Este campo BASE DE DATOS ejecutará una consulta en una base de datos y mostrará el resultado en una tabla.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Inserte otro campo BASE DE DATOS con una consulta más compleja que ordene todos los productos en orden descendente por ventas brutas.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Estas propiedades tienen la misma función que las cláusulas LIMIT y TOP.
// Configúrelos para mostrar solo las filas 1 a 10 del resultado de la consulta en la tabla del campo.
field.FirstRecord = "1";
field.LastRecord = "10";

Esta propiedad es el índice del formato que queremos usar para nuestra tabla. La lista de formatos de tabla se encuentra en el menú "Autoformato de tabla..."
// que aparece al crear un campo de BASE DE DATOS en Microsoft Word. El índice 10 corresponde al formato "Colorful 3".
field.TableFormat = "10";

// La propiedad FormatAttribute es una representación de cadena de un entero que almacena múltiples indicadores.
//Podemos aplicar de forma patriarcal el formato al que apunta la propiedad TableFormat estableciendo diferentes indicadores en esta propiedad.
// El número que utilizamos es la suma de una combinación de valores correspondientes a diferentes aspectos del estilo de la tabla.
// 63 representa 1 (bordes) + 2 (sombreado) + 4 (fuente) + 8 (color) + 16 (ajuste automático) + 32 (filas de encabezado).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Ver también

* class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* class [FieldDatabase](../../fielddatabase/)
* interface [IFieldDatabaseProvider](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
