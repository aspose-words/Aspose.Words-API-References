---
title: FontSavingArgs Class
linktitle: FontSavingArgs
articleTitle: FontSavingArgs
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.FontSavingArgs class—enhance document processing with detailed FontSaving event data for superior customization and control.
type: docs
weight: 5770
url: /net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Provides data for the [`FontSaving`](../ifontsavingcallback/fontsaving/) event.

To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.

```csharp
public class FontSavingArgs
```

## Properties

| Name | Description |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Indicates whether the current font is bold. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Gets the document object that is being saved. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Indicates the current font family name. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Gets or sets the file name (without path) where the font will be saved to. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Allows to specify the stream where the font will be saved to. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Allows to specify whether the current font will be exported as a font resource. Default is `true`. |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Allows to specify whether the current font will be subsetted before exporting as a font resource. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Indicates whether the current font is italic. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Specifies whether Aspose.Words should keep the stream open or close it after saving a font. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Gets the original font file name with an extension. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Gets the original font file size. |

## Remarks

When Aspose.Words saves a document to HTML or related formats and [`ExportFontResources`](../htmlsaveoptions/exportfontresources/) is set to `true`, it saves each font subject for export into a separate file.

`FontSavingArgs` controls whether particular font resource should be exported and how.

`FontSavingArgs` also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

To decide whether to save a particular font resource, use the [`IsExportNeeded`](./isexportneeded/) property.

To save fonts into streams instead of files, use the [`FontStream`](./fontstream/) property.

## Examples

Shows how to define custom logic for exporting fonts when saving to HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Configure a SaveOptions object to export fonts to separate files.
    // Set a callback that will handle font saving in a custom manner.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // The callback will export .ttf files and save them alongside the output document.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
        Console.WriteLine(fontFilename);

}

/// <summary>
/// Prints information about exported fonts and saves them in the same local system folder as their output .html.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // We can also access the source document from here.
        Assert.That(args.Document.OriginalFileName.EndsWith("Rendering.docx"), Is.True);

        Assert.That(args.IsExportNeeded, Is.True);
        Assert.That(args.IsSubsettingNeeded, Is.True);

        // There are two ways of saving an exported font.
        // 1 -  Save it to a local file system location:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 -  Save it to a stream:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.That(args.KeepFontStreamOpen, Is.False);
    }
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
