---
title: Table.FirstRow
second_title: Referencia de API de Aspose.Words para .NET
description: Table propiedad. Devuelve el primeroRow nodo en la tabla.
type: docs
weight: 160
url: /es/net/aspose.words.tables/table/firstrow/
---
## Table.FirstRow property

Devuelve el primero[`Row`](../../row/) nodo en la tabla.

```csharp
public Row FirstRow { get; }
```

### Ejemplos

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

Muestra cómo combinar las filas de dos tablas en una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// A continuación se muestran dos formas de obtener una tabla de un documento.
// 1 - De la colección "Tablas" de un nodo Cuerpo:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Usando el método "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Agrega todas las filas de la tabla actual a la siguiente.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Elimina el contenedor de la tabla vacía.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Ver también

* class [Row](../../row/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../table/)
* asamblea [Aspose.Words](../../../)


