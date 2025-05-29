---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlSaveOptions ExportTextInputFormFieldAsText optimiza los campos de formulario de entrada de texto para un almacenamiento HTML o MHTML sin interrupciones. ¡Mejore su proceso de exportación!
type: docs
weight: 260
url: /es/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Controla cómo se guardan los campos del formulario de entrada de texto en HTML o MHTML. El valor predeterminado es`FALSO` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Observaciones

Cuando se establece en`verdadero` , exporta los campos del formulario de entrada de texto como texto normal. Cuando`FALSO`, exporta campos de formulario de ingreso de texto de Word como elementos INPUT en HTML.

Al exportar a EPUB, los campos del formulario de entrada de texto siempre se guardan como texto debido a los requisitos de este formato.

## Ejemplos

Muestra cómo especificar la carpeta para almacenar las imágenes vinculadas después de guardarlas en .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Establezca una opción para exportar los campos de formulario como texto simple en lugar de elementos de entrada HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
