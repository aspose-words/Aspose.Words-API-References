---
title: Document.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words para .NET
description: Optimice su documento con el método NormalizeFieldTypes, garantizando que todos los valores de tipo de campo se alineen con los códigos de campo para lograr una mayor consistencia y precisión.
type: docs
weight: 670
url: /es/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Cambia los valores del tipo de campo[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) en todo el documento para que correspondan a los tipos de campo contenidos en los códigos de campo.

```csharp
public void NormalizeFieldTypes()
```

## Observaciones

Utilice este método después de realizar cambios en el documento que afecten los tipos de campo.

Para cambiar los valores del tipo de campo en una parte específica del documento, utilice[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

## Ejemplos

Muestra cómo mantener actualizado el tipo de un campo con su código de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words detecta automáticamente los tipos de campo según los códigos de campo.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Cambia manualmente el texto sin formato del campo, que determina el código del campo.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// Cambiar el código de campo ha cambiado este campo a uno de un tipo diferente,
// pero las propiedades de tipo del campo todavía muestran el tipo antiguo.
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
