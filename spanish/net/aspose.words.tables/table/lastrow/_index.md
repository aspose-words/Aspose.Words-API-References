---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words para .NET
description: Descubra la propiedad LastRow de la tabla para acceder fácilmente al nodo Fila final de su tabla, mejorando la gestión y la eficiencia de los datos.
type: docs
weight: 180
url: /es/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Devuelve el último[`Row`](../../row/) nodo en la tabla.

```csharp
public Row LastRow { get; }
```

## Ejemplos

Muestra cómo eliminar la primera y la última fila de todas las tablas de un documento.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

### Ver también

* class [Row](../../row/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
