---
title: XamlFlowSaveOptions.XamlFlowSaveOptions
second_title: Aspose.Words für .NET-API-Referenz
description: XamlFlowSaveOptions constructeur. Initialisiert eine neue Instanz dieser Klasse die zum Speichern eines Dokuments im verwendet werden kannXamlFlow format.
type: docs
weight: 10
url: /de/net/aspose.words.saving/xamlflowsaveoptions/xamlflowsaveoptions/
---
## XamlFlowSaveOptions() {#constructor}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannXamlFlow format.

```csharp
public XamlFlowSaveOptions()
```

### Beispiele

Zeigt, wie die Dateinamen von verknüpften Bildern gedruckt werden, die beim Konvertieren eines Dokuments in Flow-Form-XAML-Dateien erstellt wurden.

```csharp
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

    // Verwenden Sie die Eigenschaft "ImagesFolderAlias", um diesen Ordner zu verwenden
    // beim Erstellen von Bild-URIs anstelle des Namens des Bildordners.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Ein durch "ImagesFolderAlias" angegebener Ordner muss die Ressourcen anstelle von "ImagesFolder" enthalten.
    // Wir müssen sicherstellen, dass der Ordner existiert, bevor die Streams des Callbacks ihre Ressourcen darin ablegen können.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// Zählt und druckt Dateinamen von Bildern, während ihr übergeordnetes Dokument in Flow-Form .xaml konvertiert wird.
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

        // Wenn wir einen Bildordner-Alias angeben, benötigen wir auch
        // Um jeden Stream umzuleiten, um sein Bild in den Alias-Ordner zu legen.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Siehe auch

* class [XamlFlowSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* Montage [Aspose.Words](../../../)

---

## XamlFlowSaveOptions(SaveFormat) {#constructor_1}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannXamlFlow oderXamlFlowPack format.

```csharp
public XamlFlowSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | SaveFormat | Kann seinXamlFlow oderXamlFlowPack. |

### Beispiele

Zeigt, wie die Dateinamen von verknüpften Bildern gedruckt werden, die beim Konvertieren eines Dokuments in Flow-Form-XAML-Dateien erstellt wurden.

```csharp
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

    // Verwenden Sie die Eigenschaft "ImagesFolderAlias", um diesen Ordner zu verwenden
    // beim Erstellen von Bild-URIs anstelle des Namens des Bildordners.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Ein durch "ImagesFolderAlias" angegebener Ordner muss die Ressourcen anstelle von "ImagesFolder" enthalten.
    // Wir müssen sicherstellen, dass der Ordner existiert, bevor die Streams des Callbacks ihre Ressourcen darin ablegen können.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// Zählt und druckt Dateinamen von Bildern, während ihr übergeordnetes Dokument in Flow-Form .xaml konvertiert wird.
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

        // Wenn wir einen Bildordner-Alias angeben, benötigen wir auch
        // Um jeden Stream umzuleiten, um sein Bild in den Alias-Ordner zu legen.
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
* namensraum [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* Montage [Aspose.Words](../../../)


