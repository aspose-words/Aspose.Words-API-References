---
title: HtmlSaveOptions.ExportFontsAsBase64
linktitle: ExportFontsAsBase64
articleTitle: ExportFontsAsBase64
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlSaveOptions ExportFontsAsBase64 mejora su HTML al integrar fuentes en codificación Base64 para un mejor rendimiento. Valor predeterminado falso.
type: docs
weight: 150
url: /es/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Especifica si los recursos de fuentes deben incrustarse en HTML en codificación Base64. El valor predeterminado es`FALSO` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

## Observaciones

De forma predeterminada, las fuentes se escriben en archivos separados. Si esta opción está configurada en`verdadero`Las fuentes se incrustarán en el CSS del documento en codificación Base64.

## Ejemplos

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
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
