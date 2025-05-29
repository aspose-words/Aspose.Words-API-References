---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words för .NET
description: Upptäck XamlFlowSaveOptions ImagesFolderAlias-egenskap för att anpassa bild-URI-sökvägar i XAML-dokument. Förbättra dina projekt med lätthet!
type: docs
weight: 40
url: /sv/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett XAML-dokument. Standardvärdet är en tom sträng.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) I XAML-format behöver Aspose.Words spara alla -bilder som är inbäddade i dokumentet som fristående filer.[`ImagesFolder`](../imagesfolder/) låter dig ange var bilderna ska sparas och`ImagesFolderAlias` låter dig ange hur bildens URI:er ska konstrueras.

Om`ImagesFolderAlias` inte är en tom sträng, så kommer bild-URI:n written till XAML att varaImagesFolderAlias + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias` är en tom sträng, så kommer bild-URI:n som skrivs till XAML att varaImagesFolder + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias` är satt till '.' (punkt), så kommer bildfilnamnet att skrivas till XAML utan sökväg oavsett andra alternativ.

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
