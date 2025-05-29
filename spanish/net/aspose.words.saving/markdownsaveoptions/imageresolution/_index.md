---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words para .NET
description: Optimice sus exportaciones de Markdown con la propiedad ImageResolution, configurando resoluciones de salida personalizadas para obtener imágenes más nítidas. El valor predeterminado es 96 ppp.
type: docs
weight: 60
url: /es/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

Especifica la resolución de salida de las imágenes al exportar a Markdown. El valor predeterminado es`96 ppp` .

```csharp
public int ImageResolution { get; set; }
```

## Ejemplos

Muestra cómo configurar la resolución de salida para las imágenes.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### Ver también

* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
