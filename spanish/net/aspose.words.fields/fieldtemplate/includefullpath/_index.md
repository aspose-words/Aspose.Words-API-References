---
title: FieldTemplate.IncludeFullPath
second_title: Referencia de API de Aspose.Words para .NET
description: FieldTemplate propiedad. Obtiene o establece si se debe incluir el nombre completo de la ruta del archivo.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

Obtiene o establece si se debe incluir el nombre completo de la ruta del archivo.

```csharp
public bool IncludeFullPath { get; set; }
```

### Ejemplos

Muestra cómo utilizar un campo PLANTILLA para mostrar la ubicación del sistema de archivos local de la plantilla de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Podemos establecer un nombre de plantilla usando los campos. Esta propiedad se utiliza cuando "doc.AttachedTemplate" está vacío.
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

* class [FieldTemplate](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldtemplate/)
* asamblea [Aspose.Words](../../../)


