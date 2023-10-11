---
title: Document.NormalizeFieldTypes
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Cambia los valores del tipo de campoFieldType deFieldStart FieldSeparator FieldEnd en todo el documento para que correspondan a los tipos de campo contenidos en los códigos de campo.
type: docs
weight: 650
url: /es/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Cambia los valores del tipo de campo[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) en todo el documento para que correspondan a los tipos de campo contenidos en los códigos de campo.

```csharp
public void NormalizeFieldTypes()
```

### Observaciones

Utilice este método después de cambios en el documento que afecten a los tipos de campos.

Para cambiar los valores de tipo de campo en una parte específica del uso del documento[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

### Ejemplos

Muestra cómo mantener actualizado el tipo de campo con su código de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words detecta automáticamente los tipos de campos según los códigos de campo.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Cambia manualmente el texto sin formato del campo, lo que determina el código del campo.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// Cambiar el código de campo ha cambiado este campo a uno de un tipo diferente,
// pero las propiedades de tipo del campo aún muestran el tipo anterior.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Actualice esas propiedades con este método para mostrar el valor actual.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType); 
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


