---
title: Table.Rows
linktitle: Rows
articleTitle: Rows
second_title: Aspose.Words para .NET
description: Acceda a las filas de la tabla sin esfuerzo con nuestra propiedad escrita, lo que garantiza una gestión de datos perfecta y una mejor organización para sus proyectos.
type: docs
weight: 260
url: /es/net/aspose.words.tables/table/rows/
---
## Table.Rows property

Proporciona acceso tipificado a las filas de la tabla.

```csharp
public RowCollection Rows { get; }
```

## Ejemplos

Muestra cómo combinar las filas de dos tablas en una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

A continuación se muestran dos formas de obtener una tabla de un documento.
// 1 - De la colección "Tablas" de un nodo Cuerpo:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Usando el método "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Agrega todas las filas de la tabla actual a la siguiente.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

//Eliminar el contenedor de tabla vacío.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

Muestra cómo iterar a través de todas las tablas del documento e imprimir el contenido de cada celda.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Podemos usar el método "ToArray" en una colección de filas para clonarla en una matriz.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Podemos usar el método "ToArray" en una colección de celdas para clonarla en una matriz.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

### Ver también

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
