---
title: TableCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words para .NET
description: Convierta sin esfuerzo su TableCollection en una matriz con el método ToArray, simplificando la gestión de datos y mejorando el rendimiento de su aplicación.
type: docs
weight: 20
url: /es/net/aspose.words.tables/tablecollection/toarray/
---
## TableCollection.ToArray method

Copia todas las tablas de la colección a una nueva matriz de tablas.

```csharp
public Table[] ToArray()
```

### Valor_devuelto

Una serie de tablas.

## Ejemplos

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

* class [Table](../../table/)
* class [TableCollection](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
