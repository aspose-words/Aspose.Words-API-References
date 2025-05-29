---
title: XamlFlowSaveOptions
linktitle: XamlFlowSaveOptions
articleTitle: XamlFlowSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck XamlFlowSaveOptions-konstruktorn för att enkelt initiera och spara dokument i XamlFlow-formatet. Förbättra ditt arbetsflöde idag!
type: docs
weight: 10
url: /sv/net/aspose.words.saving/xamlflowsaveoptions/xamlflowsaveoptions/
---
## XamlFlowSaveOptions() {#constructor}

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iXamlFlow format.

```csharp
public XamlFlowSaveOptions()
```

## Exempel

Visar hur man skriver ut filnamnen på länkade bilder som skapats vid konvertering av ett dokument till flödesformat .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Skapa ett "XamlFlowSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur vi sparar dokumentet till XAML-formatet.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Använd egenskapen "ImagesFolder" för att tilldela en mapp i det lokala filsystemet till vilken
    // Aspose.Words sparar alla länkade bilder i dokumentet.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Använd egenskapen "ImagesFolderAlias" för att använda den här mappen
    // när man konstruerar bild-URI:er istället för bildmappens namn.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // En mapp som anges av "ImagesFolderAlias" måste innehålla resurserna istället för "ImagesFolder".
    // Vi måste säkerställa att mappen finns innan återanropets strömmar kan lägga sina resurser i den.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Räknar och skriver ut filnamn på bilder medan deras överordnade dokument konverteras till flödesformat .xaml.
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

        // Om vi angav ett alias för bildmappen skulle vi också behöva
        // för att omdirigera varje ström för att lägga dess bild i alias-mappen.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Se även

* class [XamlFlowSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## XamlFlowSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iXamlFlow ellerXamlFlowPack format.

```csharp
public XamlFlowSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | SaveFormat | Kan varaXamlFlow ellerXamlFlowPack. |

## Exempel

Visar hur man skriver ut filnamnen på länkade bilder som skapats vid konvertering av ett dokument till flödesformat .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Skapa ett "XamlFlowSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur vi sparar dokumentet till XAML-formatet.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Använd egenskapen "ImagesFolder" för att tilldela en mapp i det lokala filsystemet till vilken
    // Aspose.Words sparar alla länkade bilder i dokumentet.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Använd egenskapen "ImagesFolderAlias" för att använda den här mappen
    // när man konstruerar bild-URI:er istället för bildmappens namn.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // En mapp som anges av "ImagesFolderAlias" måste innehålla resurserna istället för "ImagesFolder".
    // Vi måste säkerställa att mappen finns innan återanropets strömmar kan lägga sina resurser i den.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Räknar och skriver ut filnamn på bilder medan deras överordnade dokument konverteras till flödesformat .xaml.
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

        // Om vi angav ett alias för bildmappen skulle vi också behöva
        // för att omdirigera varje ström för att lägga dess bild i alias-mappen.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XamlFlowSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
