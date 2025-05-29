---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar la propiedad ShadeFormData para mejorar la visibilidad del formulario con sombreado gris, mejorando la experiencia del usuario y la accesibilidad.
type: docs
weight: 400
url: /es/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Especifica si se debe activar el sombreado gris en los campos de formulario.

```csharp
public bool ShadeFormData { get; set; }
```

## Ejemplos

Muestra cómo aplicar sombreado gris a los campos de formulario.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

//Podemos desactivar el sombreado gris, para que el texto marcado se mezcle con el resto del texto.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
