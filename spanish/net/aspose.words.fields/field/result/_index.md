---
title: Field.Result
second_title: Referencia de API de Aspose.Words para .NET
description: Field propiedad. Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo.
type: docs
weight: 70
url: /es/net/aspose.words.fields/field/result/
---
## Field.Result property

Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo.

```csharp
public string Result { get; set; }
```

### Ejemplos

Muestra cómo insertar un campo en un documento utilizando un código de campo.

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

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../field/)
* asamblea [Aspose.Words](../../../)


