---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldChar FieldType, que revela el tipo de campo, optimizando la gestión de datos y la eficiencia de su programación. ¡Obtenga más información ahora!
type: docs
weight: 10
url: /es/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Devuelve el tipo del campo.

```csharp
public FieldType FieldType { get; }
```

## Ejemplos

Muestra cómo trabajar con un nodo FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Recupera el objeto de fachada que representa el campo en el documento.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

//Actualiza el campo para mostrar la fecha actual.
field.Update();
```

### Ver también

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
