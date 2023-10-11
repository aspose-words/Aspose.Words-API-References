---
title: Field.Type
second_title: Referencia de API de Aspose.Words para .NET
description: Field propiedad. Obtiene el tipo de campo de Microsoft Word.
type: docs
weight: 100
url: /es/net/aspose.words.fields/field/type/
---
## Field.Type property

Obtiene el tipo de campo de Microsoft Word.

```csharp
public virtual FieldType Type { get; }
```

### Ejemplos

Muestra cómo insertar un campo en un documento usando un código de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Ver también

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../field/)
* asamblea [Aspose.Words](../../../)


