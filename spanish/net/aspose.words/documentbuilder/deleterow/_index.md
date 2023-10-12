---
title: DocumentBuilder.DeleteRow
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Elimina una fila de una tabla.
type: docs
weight: 200
url: /es/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Elimina una fila de una tabla.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| tableIndex | Int32 | El índice de la tabla. |
| rowIndex | Int32 | El índice de la fila de la tabla. |

### Valor_devuelto

El nodo de fila que se acaba de eliminar.

### Observaciones

Si el cursor está dentro de la fila que se está eliminando, el cursor se mueve a la siguiente fila o al siguiente párrafo después de la tabla.

Si elimina una fila de una tabla que contiene solo una fila, se elimina toda la tabla .

Para los parámetros de índice, cuando el índice es mayor o igual a 0, especifica un índice desde el comienzo siendo 0 el primer elemento. Cuando el índice es menor que 0, especifica un índice desde al final, siendo -1 el último elemento.

### Ejemplos

Muestra cómo eliminar una fila de una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// Elimina la primera fila de la primera tabla del documento.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Ver también

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


