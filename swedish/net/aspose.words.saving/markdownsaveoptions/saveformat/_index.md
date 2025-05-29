---
title: MarkdownSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SaveFormat i MarkdownSaveOptions för att enkelt spara dokument i Markdown-format, vilket säkerställer kompatibilitet och användarvänlighet.
type: docs
weight: 130
url: /sv/net/aspose.words.saving/markdownsaveoptions/saveformat/
---
## MarkdownSaveOptions.SaveFormat property

Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaMarkdown .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Exempel

Visar hur man byter namn på bilden när den sparas i Markdown-dokumentet.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Om vi konverterar ett dokument som innehåller bilder till Markdown, kommer vi att få en Markdown-fil som länkar till flera bilder.
    // Varje bild kommer att vara i form av en fil i det lokala filsystemet.
    // Det finns också en återanropsfunktion som kan anpassa namn och filsystemplats för varje bild.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // Metoden ImageSaving() för vår återanropning kommer att köras vid denna tidpunkt.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// Byter namn på sparade bilder som skapas när ett Markdown-dokument sparas.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        args.ImageFileName = imageFileName;
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
