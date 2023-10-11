---
title: Row.EnsureMinimum
second_title: Referencia de API de Aspose.Words para .NET
description: Row método. Si elRow no tiene celdas crea y agrega unaCell .
type: docs
weight: 150
url: /es/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Si el[`Row`](../) no tiene celdas, crea y agrega una[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

### Ejemplos

Muestra cómo garantizar que un nodo de fila contenga los nodos que necesitamos para comenzar a agregarle contenido.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Las filas contienen celdas que contienen párrafos con elementos típicos como ejecuciones, formas e incluso otras tablas.
// Nuestra nueva fila no tiene ninguno de estos nodos y no podemos agregarle contenido hasta que los tenga.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Llamar al método "EnsureMinimum" en una tabla garantizará que
// la tabla tiene al menos una celda con un párrafo vacío.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ver también

* class [Row](../)
* espacio de nombres [Aspose.Words.Tables](../../row/)
* asamblea [Aspose.Words](../../../)


