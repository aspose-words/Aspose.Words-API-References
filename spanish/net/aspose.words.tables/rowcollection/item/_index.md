---
title: RowCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda a cualquier fila fácilmente con la propiedad Elemento de RowCollection. Recupere datos rápidamente en el índice deseado para una gestión de datos fluida.
type: docs
weight: 10
url: /es/net/aspose.words.tables/rowcollection/item/
---
## RowCollection indexer

Recupera una[`Row`](../../row/) en el índice dado.

```csharp
public Row this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice de la colección. |

## Observaciones

El índice está basado en cero.

Se permiten índices negativos e indican acceso desde la parte posterior de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos de la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que la cantidad de elementos de la lista, esto devuelve una referencia nula.

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

* class [Row](../../row/)
* class [RowCollection](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
