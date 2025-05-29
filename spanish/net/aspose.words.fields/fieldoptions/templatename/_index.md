---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldOptions TemplateName para administrar fácilmente el nombre del archivo de plantilla de su documento para una mejor organización y eficiencia.
type: docs
weight: 190
url: /es/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Obtiene o establece el nombre de archivo de la plantilla utilizada por el documento.

```csharp
public string TemplateName { get; set; }
```

## Observaciones

Esta propiedad es utilizada por el[`FieldTemplate`](../../fieldtemplate/) campo si el[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) La propiedad está vacía.

Si esta propiedad está vacía, el nombre del archivo de plantilla predeterminado`Normal.dotm` se utiliza

## Ejemplos

Muestra cómo utilizar un campo PLANTILLA para mostrar la ubicación del sistema de archivos local de la plantilla de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Podemos establecer un nombre de plantilla mediante los campos. Esta propiedad se utiliza cuando el campo "doc.AttachedTemplate" está vacío.
// Si esta propiedad está vacía, se utiliza el nombre de archivo de plantilla predeterminado "Normal.dotm".
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### Ver también

* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
