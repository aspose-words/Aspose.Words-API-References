---
title: FontSavingArgs.IsExportNeeded
linktitle: IsExportNeeded
articleTitle: IsExportNeeded
second_title: Aspose.Words for .NET
description: Discover the FontSavingArgs IsExportNeeded property to control font resource exports. Maximize efficiency with customizable settings for your projects!
type: docs
weight: 60
url: /net/aspose.words.saving/fontsavingargs/isexportneeded/
---
## FontSavingArgs.IsExportNeeded property

Allows to specify whether the current font will be exported as a font resource. Default is `true`.

```csharp
public bool IsExportNeeded { get; set; }
```

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

* class [FontSavingArgs](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
