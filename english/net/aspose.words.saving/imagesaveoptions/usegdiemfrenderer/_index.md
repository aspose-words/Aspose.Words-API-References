---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words for .NET
description: Optimize EMF saving with ImageSaveOptions. Control GDI or Aspose.Words renderer settings for enhanced image quality and performance.
type: docs
weight: 200
url: /net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Remarks

If set to `true` GDI+ metafile renderer is used. I.e. content is written to GDI+ graphics object and saved to metafile.

If set to `false` Aspose.Words metafile renderer is used. I.e. content is written directly to the metafile format with Aspose.Words.

Has effect only when saving to EMF.

GDI+ saving works only on .NET.

The default value is `true`.

## Examples

Shows how to choose a renderer when converting a document to .emf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// When we save the document as an EMF image, we can pass a SaveOptions object to select a renderer for the image.
// If we set the "UseGdiEmfRenderer" flag to "true", Aspose.Words will use the GDI+ renderer.
// If we set the "UseGdiEmfRenderer" flag to "false", Aspose.Words will use its own metafile renderer.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### See Also

* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
