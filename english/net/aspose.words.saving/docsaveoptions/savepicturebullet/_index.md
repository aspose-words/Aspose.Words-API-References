---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words for .NET
description: Discover how the DocSaveOptions SavePictureBullet property enhances your document output. Control PictureBullet data saving effortlessly for optimal results.
type: docs
weight: 60
url: /net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

When `false`, PictureBullet data is not saved to output document. Default value is `true`.

```csharp
public bool SavePictureBullet { get; set; }
```

## Remarks

This option is provided for Word 97, which cannot work correctly with PictureBullet data. To remove PictureBullet data, set the option to "false".

## Examples

Shows how to omit PictureBullet data from the document when saving.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Some word processors, such as Microsoft Word 97, are incompatible with PictureBullet data.
// By setting a flag in the SaveOptions object,
// we can convert all image bullet points to ordinary bullet points while saving.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### See Also

* class [DocSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
