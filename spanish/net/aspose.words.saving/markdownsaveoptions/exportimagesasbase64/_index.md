---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad MarkdownSaveOptions ExportImagesAsBase64 mejora sus archivos de salida al permitir guardar imágenes en formato Base64. Valor predeterminado falso.
type: docs
weight: 40
url: /es/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Especifica si las imágenes se guardan en formato Base64 en el archivo de salida. El valor predeterminado es`FALSO` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Observaciones

Cuando esta propiedad se establece en`verdadero` Los datos de las imágenes se exportan directamente a la**imagen** No se crean elementos ni archivos separados.

## Ejemplos

Muestra cómo guardar un documento .md con imágenes incrustadas en su interior.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### Ver también

* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
