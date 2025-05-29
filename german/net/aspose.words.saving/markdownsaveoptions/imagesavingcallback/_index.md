---
title: MarkdownSaveOptions.ImageSavingCallback
linktitle: ImageSavingCallback
articleTitle: ImageSavingCallback
second_title: Aspose.Words für .NET
description: Steuern Sie die Bildspeicherung in Markdown mit dem ImageSavingCallback von MarkdownSaveOptions. Verbessern Sie die Dokumentformatierung und optimieren Sie Ihren Workflow mühelos!
type: docs
weight: 70
url: /de/net/aspose.words.saving/markdownsaveoptions/imagesavingcallback/
---
## MarkdownSaveOptions.ImageSavingCallback property

Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument in gespeichert wird.Markdown format.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

## Beispiele

Zeigt, wie der Bildname beim Speichern in einem Markdown-Dokument umbenannt wird.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Wenn wir ein Dokument, das Bilder enthält, in Markdown konvertieren, erhalten wir am Ende eine Markdown-Datei, die auf mehrere Bilder verweist.
    // Jedes Bild liegt in Form einer Datei im lokalen Dateisystem vor.
    // Es gibt auch einen Rückruf, mit dem der Name und der Dateisystemspeicherort jedes Bildes angepasst werden können.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // Zu diesem Zeitpunkt wird die Methode ImageSaving() unseres Rückrufs ausgeführt.
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
/// Benennt gespeicherte Bilder um, die beim Speichern eines Markdown-Dokuments erstellt werden.
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

### Siehe auch

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
