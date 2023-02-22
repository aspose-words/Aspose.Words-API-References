---
title: Document.ShadeFormData
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Especifica si se debe activar el sombreado gris en los campos de formulario.
type: docs
weight: 360
url: /es/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Especifica si se debe activar el sombreado gris en los campos de formulario.

```csharp
public bool ShadeFormData { get; set; }
```

### Ejemplos

Muestra cómo aplicar sombreado gris a los campos de formulario.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Podemos desactivar el sombreado gris, por lo que el texto marcado se mezclará con el otro texto.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


