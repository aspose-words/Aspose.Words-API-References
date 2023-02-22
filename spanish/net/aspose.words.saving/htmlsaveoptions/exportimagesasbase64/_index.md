---
title: HtmlSaveOptions.ExportImagesAsBase64
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica si las imágenes se guardan en formato Base64 en la salida HTML MHTML o EPUB. El valor predeterminado esfalso .
type: docs
weight: 180
url: /es/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Especifica si las imágenes se guardan en formato Base64 en la salida HTML, MHTML o EPUB. El valor predeterminado es`falso` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

### Observaciones

Cuando esta propiedad se establece en`verdadero`los datos de las imágenes se exportan directamente al **imagen** no se crean elementos ni archivos separados.

### Ejemplos

Muestra cómo incrustar fuentes dentro de un documento HTML guardado.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontsAsBase64 = true,
    CssStyleSheetType = CssStyleSheetType.Embedded,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

Muestra cómo guardar un documento .html con imágenes incrustadas en su interior.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportImagesAsBase64 = exportImagesAsBase64,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("<img src=\"data:image/png;base64")
    : outDocContents.Contains("<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


