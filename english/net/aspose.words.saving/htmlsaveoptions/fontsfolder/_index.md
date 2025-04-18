---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words for .NET
description: Discover the HtmlSaveOptions FontsFolder property to easily manage font storage for HTML exports, enhancing document presentation and accessibility.
type: docs
weight: 310
url: /net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string.

```csharp
public string FontsFolder { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in HTML format and [`ExportFontResources`](../exportfontresources/) is set to `true`, Aspose.Words needs to save fonts used in the document as standalone files. `FontsFolder` allows you to specify where the fonts will be saved and [`FontsFolderAlias`](../fontsfolderalias/) allows to specify how the font URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the fonts in the same folder where the document file is saved. Use `FontsFolder` to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the fonts, but still needs to save the fonts somewhere. In this case, you need to specify an accessible folder in the `FontsFolder` property or provide custom streams via the [`FontSavingCallback`](../fontsavingcallback/) event handler.

If the folder specified by `FontsFolder` doesn't exist, it will be created automatically.

[`ResourceFolder`](../resourcefolder/) is another way to specify a folder where fonts should be saved.

## Examples

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
