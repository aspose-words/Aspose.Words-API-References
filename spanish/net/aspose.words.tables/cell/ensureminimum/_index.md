---
title: Cell.EnsureMinimum
second_title: Referencia de API de Aspose.Words para .NET
description: Cell método. Si el último elemento secundario no es un párrafo crea y agrega un párrafo vacío.
type: docs
weight: 120
url: /es/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Si el último elemento secundario no es un párrafo, crea y agrega un párrafo vacío.

```csharp
public void EnsureMinimum()
```

### Ejemplos

Muestra cómo garantizar que un nodo de celda contenga los nodos que necesitamos para comenzar a agregarle contenido.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Las celdas pueden contener párrafos con elementos típicos como corridas, formas e incluso otras tablas.
// Nuestra nueva celda no tiene ningún párrafo, y no podemos agregarle contenidos como nodos de ejecución y forma hasta que lo tenga.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// Llamar al método "EnsureMinimum" en una celda asegurará que
// la celda tiene al menos un párrafo vacío, al que luego podemos agregar contenido.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ver también

* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../cell/)
* asamblea [Aspose.Words](../../../)


