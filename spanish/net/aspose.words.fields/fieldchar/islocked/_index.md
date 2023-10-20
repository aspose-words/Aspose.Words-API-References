---
title: FieldChar.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words para .NET
description: FieldChar IsLocked propiedad. Obtiene o establece si el campo principal está bloqueado no debe volver a calcular su resultado en C#.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Obtiene o establece si el campo principal está bloqueado (no debe volver a calcular su resultado).

```csharp
public bool IsLocked { get; set; }
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

// Actualiza el campo para mostrar la fecha actual.
field.Update();
```

### Ver también

* class [FieldChar](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
