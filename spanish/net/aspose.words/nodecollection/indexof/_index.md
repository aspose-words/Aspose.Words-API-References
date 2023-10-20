---
title: NodeCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words para .NET
description: NodeCollection IndexOf método. Devuelve el índice de base cero del nodo especificado en C#.
type: docs
weight: 70
url: /es/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

Devuelve el índice de base cero del nodo especificado.

```csharp
public int IndexOf(Node node)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| node | Node | El nodo a localizar. |

### Valor_devuelto

El índice de base cero del nodo dentro de la colección, si se encuentra; de lo contrario, -1.

## Observaciones

Este método realiza una búsqueda lineal; por lo tanto, el tiempo promedio de ejecución es proporcional a[`Count`](../count/).

## Ejemplos

Muestra cómo obtener el índice de un nodo en una colección.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.AreEqual(0, allTables.IndexOf(table));

Row row = table.Rows[2];

Assert.AreEqual(2, table.IndexOf(row));

Cell cell = row.LastCell;

Assert.AreEqual(4, row.IndexOf(cell));
```

### Ver también

* class [Node](../../node/)
* class [NodeCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
