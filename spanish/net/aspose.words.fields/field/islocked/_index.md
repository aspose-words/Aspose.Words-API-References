---
title: Field.IsLocked
second_title: Referencia de API de Aspose.Words para .NET
description: Field propiedad. Obtiene o establece si el campo está bloqueado no debe volver a calcular su resultado.
type: docs
weight: 50
url: /es/net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

Obtiene o establece si el campo está bloqueado (no debe volver a calcular su resultado).

```csharp
public bool IsLocked { get; set; }
```

### Ejemplos

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

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../field/)
* asamblea [Aspose.Words](../../../)


