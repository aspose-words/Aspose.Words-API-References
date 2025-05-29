---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra el tipo de campo de Microsoft Word con nuestra propiedad "Tipo de campo". Mejore sus documentos con formato preciso y funciones de contenido dinámico.
type: docs
weight: 100
url: /es/net/aspose.words.fields/field/type/
---
## Field.Type property

Obtiene el tipo de campo de Microsoft Word.

```csharp
public virtual FieldType Type { get; }
```

## Ejemplos

Muestra cómo insertar un campo en un documento utilizando un código de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Ver también

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
