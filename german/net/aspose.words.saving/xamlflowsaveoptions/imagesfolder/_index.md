---
title: XamlFlowSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words für .NET
description: XamlFlowSaveOptions ImagesFolder eigendom. Gibt den physischen Ordner an in dem Bilder gespeichert werden wenn ein Dokument in das XAMLFormat exportiert wird. Standard ist eine leere Zeichenfolge in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/xamlflowsaveoptions/imagesfolder/
---
## XamlFlowSaveOptions.ImagesFolder property

Gibt den physischen Ordner an, in dem Bilder gespeichert werden, wenn ein Dokument in das XAML-Format exportiert wird. Standard ist eine leere Zeichenfolge.

```csharp
public string ImagesFolder { get; set; }
```

## Bemerkungen

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) Im XAML-Format muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.`ImagesFolder` Mit können Sie angeben, wo die Bilder gespeichert werden[`ImagesFolderAlias`](../imagesfolderalias/) ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words die -Bilder standardmäßig im selben Ordner, in dem die Dokumentdatei gespeichert ist. Verwenden`ImagesFolder` , um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words über keinen Ordner zum Speichern der Bilder, , muss die Bilder aber trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner im angeben`ImagesFolder` Eigenschaft oder stellen Sie benutzerdefinierte Streams über bereit[`ImageSavingCallback`](../imagesavingcallback/) Ereignishandler.

## Beispiele

Zeigt, wie die Dateinamen verknüpfter Bilder gedruckt werden, die beim Konvertieren eines Dokuments in Flow-Form .xaml erstellt wurden.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Erstellen Sie ein „XamlFlowSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument im XAML-Speicherformat speichern.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Mit der Eigenschaft „ImagesFolder“ einen Ordner im lokalen Dateisystem zuweisen, in den
    // Aspose.Words speichert alle verknüpften Bilder des Dokuments.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Verwenden Sie die Eigenschaft „ImagesFolderAlias“, um diesen Ordner zu verwenden
    // beim Erstellen von Bild-URIs anstelle des Namens des Bilderordners.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Ein durch „ImagesFolderAlias“ angegebener Ordner muss die Ressourcen anstelle von „ImagesFolder“ enthalten.
    // Wir müssen sicherstellen, dass der Ordner vorhanden ist, bevor die Streams des Rückrufs ihre Ressourcen darin ablegen können.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Zählt und druckt Dateinamen von Bildern, während das übergeordnete Dokument in Flow-Form .xaml konvertiert wird.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // Wenn wir einen Bildordner-Alias angeben würden, würden wir auch Folgendes benötigen
        // um jeden Stream umzuleiten, um sein Bild im Alias-Ordner abzulegen.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Siehe auch

* class [XamlFlowSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
