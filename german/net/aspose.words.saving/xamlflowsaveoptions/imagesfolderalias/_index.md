---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImagesFolderAlias-Eigenschaft von XamlFlowSaveOptions, um Bild-URI-Pfade in XAML-Dokumenten anzupassen. Optimieren Sie Ihre Projekte ganz einfach!
type: docs
weight: 40
url: /de/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein XAML-Dokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Bemerkungen

Wenn Sie eine[`Document`](../../../aspose.words/document/) Im XAML-Format muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.[`ImagesFolder`](../imagesfolder/) ermöglicht Ihnen, festzulegen, wo die Bilder gespeichert werden und`ImagesFolderAlias` ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn`ImagesFolderAlias` ist keine leere Zeichenfolge, dann wird die Bild-URI geschrieben zu XAML wirdImagesFolderAlias + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias` ist eine leere Zeichenfolge, dann wird die Bild-URI, die in XAML geschrieben wird,ImagesFolder + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias` auf „.“ (Punkt) gesetzt ist, wird der Bilddateiname ohne Pfad in XAML geschrieben, unabhängig von anderen Optionen.

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

* class [XamlFlowSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
