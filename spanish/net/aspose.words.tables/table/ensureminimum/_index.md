---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words para .NET
description: Descubra el método Table EnsureMinimum, cree y agregue sin esfuerzo una fila cuando su tabla esté vacía para una administración de datos perfecta.
type: docs
weight: 420
url: /es/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Si la tabla no tiene filas, crea y agrega una[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Ejemplos

Muestra cómo garantizar que un nodo de tabla contenga los nodos que necesitamos para agregar contenido.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Las tablas contienen filas, que contienen celdas, que pueden contener párrafos
// con elementos típicos como carreras, formas e incluso otras tablas.
//Nuestra nueva tabla no tiene ninguno de estos nodos y no podemos agregarle contenido hasta que los tenga.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Llamar al método "EnsureMinimum" en una tabla garantizará que
//la tabla tiene al menos una fila y una celda con un párrafo vacío.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
