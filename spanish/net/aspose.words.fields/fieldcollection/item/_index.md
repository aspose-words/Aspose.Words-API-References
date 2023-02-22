---
title: FieldCollection.Item
second_title: Referencia de API de Aspose.Words para .NET
description: FieldCollection propiedad. Devuelve un campo en el índice especificado.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

Devuelve un campo en el índice especificado.

```csharp
public Field this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice de la colección. |

### Observaciones

El índice está basado en cero.

Los índices negativos están permitidos e indican el acceso desde la parte posterior de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos de la lista, esto devuelve una referencia nula.

### Ejemplos

Muestra cómo eliminar campos de una colección de campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// A continuación se muestran cuatro formas de eliminar campos de una colección de campos.
// 1 - Obtener un campo para eliminarlo:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Obtener la colección para eliminar un campo que le pasamos a su método de eliminación:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Eliminar un campo de una colección en un índice:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Elimina todos los campos de la colección a la vez:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Ver también

* class [Field](../../field/)
* class [FieldCollection](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldcollection/)
* asamblea [Aspose.Words](../../../)


