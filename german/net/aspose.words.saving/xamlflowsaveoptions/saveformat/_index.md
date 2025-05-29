---
title: XamlFlowSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveFormat-Eigenschaft von XamlFlowSaveOptions, um Ihre Dokumente einfach im XamlFlow-Format zu speichern. Optimieren Sie Ihren Workflow mit dieser wichtigen Funktion!
type: docs
weight: 60
url: /de/net/aspose.words.saving/xamlflowsaveoptions/saveformat/
---
## XamlFlowSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurXamlFlow .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Beispiele

Zeigt, wie die Dateinamen verknüpfter Bilder gedruckt werden, die beim Konvertieren eines Dokuments in das Flow-Format .xaml erstellt wurden.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Erstellen Sie ein „XamlFlowSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument im XAML-Speicherformat speichern.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Verwenden Sie die Eigenschaft "ImagesFolder", um einen Ordner im lokalen Dateisystem zuzuweisen, in den
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
/// Zählt und druckt Dateinamen von Bildern, während ihr übergeordnetes Dokument in das Flow-Format .xaml konvertiert wird.
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

        // Wenn wir einen Alias für den Bildordner angeben würden, bräuchten wir auch
        // um jeden Stream umzuleiten, um sein Bild im Alias-Ordner abzulegen.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XamlFlowSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
