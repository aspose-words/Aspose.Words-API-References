---
title: XamlFlowSaveOptions.SaveFormat
second_title: Aspose.Words för .NET API Referens
description: XamlFlowSaveOptions fast egendom. Anger formatet som dokumentet kommer att sparas i om detta sparaalternativobjekt används. Kan endastXamlFlow .
type: docs
weight: 50
url: /sv/net/aspose.words.saving/xamlflowsaveoptions/saveformat/
---
## XamlFlowSaveOptions.SaveFormat property

Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endastXamlFlow .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Exempel

Visar hur man skriver ut filnamnen på länkade bilder som skapats när ett dokument konverteras till flödesformat .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Skapa ett "XamlFlowSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
    // för att ändra hur vi sparar dokumentet till XAML-sparformatet.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Använd egenskapen "ImagesFolder" för att tilldela en mapp i det lokala filsystemet som
    // Aspose.Words kommer att spara alla dokumentets länkade bilder.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Använd egenskapen "ImagesFolderAlias" för att använda den här mappen
    // när du konstruerar bild-URI:er istället för bildmappens namn.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // En mapp specificerad av "ImagesFolderAlias" kommer att behöva innehålla resurserna istället för "ImagesFolder".
    // Vi måste se till att mappen finns innan återuppringningens strömmar kan lägga sina resurser i den.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Räknar och skriver ut filnamn på bilder medan deras överordnade dokument konverteras till flödesformen .xaml.
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

        // Om vi angav ett bildmappalias skulle vi också behöva
        // för att omdirigera varje ström för att placera dess bild i aliasmappen.
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
* namnutrymme [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* hopsättning [Aspose.Words](../../../)


