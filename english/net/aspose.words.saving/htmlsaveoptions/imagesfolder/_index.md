---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words for .NET
description: Discover HtmlSaveOptions ImagesFolder property. Easily set the folder for saving images when exporting documents to HTML. Streamline your workflow today!
type: docs
weight: 360
url: /net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string.

```csharp
public string ImagesFolder { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. `ImagesFolder` allows you to specify where the images will be saved and [`ImagesFolderAlias`](../imagesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use `ImagesFolder` to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the `ImagesFolder` property or provide custom streams via the [`ImageSavingCallback`](../imagesavingcallback/) event handler.

If the folder specified by `ImagesFolder` doesn't exist, it will be created automatically.

[`ResourceFolder`](../resourcefolder/) is another way to specify a folder where images should be saved.

## Examples

Shows how to specify the folder for storing linked images after saving to .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Set an option to export form fields as plain text instead of HTML input elements.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
