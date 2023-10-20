---
title: FieldCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words para .NET
description: FieldCollection Remove método. Elimina el campo especificado de esta colección y del documento en C#.
type: docs
weight: 50
url: /es/net/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection.Remove method

Elimina el campo especificado de esta colección y del documento.

```csharp
public void Remove(Field field)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| field | Field | Un campo para eliminar. |

## Ejemplos

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
// 1 - Obtener un campo para eliminarse a sí mismo:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Obtener la colección para eliminar un campo que pasamos a su método de eliminación:
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
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
