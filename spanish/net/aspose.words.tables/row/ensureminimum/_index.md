---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words para .NET
description: Descubra el método Row EnsureMinimum, cree y agregue sin esfuerzo una celda cuando no existe ninguna, mejorando la gestión de su estructura de datos.
type: docs
weight: 150
url: /es/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Si el[`Row`](../) No tiene celdas, crea y agrega una.[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

## Ejemplos

Muestra cómo garantizar que un nodo de fila contenga los nodos que necesitamos para comenzar a agregarle contenido.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Las filas contienen celdas que contienen párrafos con elementos típicos como carreras, formas e incluso otras tablas.
//Nuestra nueva fila no tiene ninguno de estos nodos y no podemos agregarle contenido hasta que los tenga.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Llamar al método "EnsureMinimum" en una tabla garantizará que
//la tabla tiene al menos una celda con un párrafo vacío.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ver también

* class [Row](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
