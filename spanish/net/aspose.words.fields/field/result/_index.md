---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words para .NET
description: Gestione fácilmente las propiedades de los resultados de campo. Acceda o modifique el texto entre los separadores de campo para optimizar la gestión de datos y mejorar la eficiencia.
type: docs
weight: 70
url: /es/net/aspose.words.fields/field/result/
---
## Field.Result property

Obtiene o establece el texto que está entre el separador de campo y el final del campo.

```csharp
public string Result { get; set; }
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

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
