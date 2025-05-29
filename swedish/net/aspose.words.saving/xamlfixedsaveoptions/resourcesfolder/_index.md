---
title: XamlFixedSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen XamlFixedSaveOptions ResourcesFolder förbättrar dokumentexport genom att definiera var bilder och teckensnitt lagras i Xaml-format.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/
---
## XamlFixedSaveOptions.ResourcesFolder property

Anger den fysiska mappen där resurser (bilder och teckensnitt) sparas när ett dokument exporteras till fast sidformat i XAML. Standard är`null` .

```csharp
public string ResourcesFolder { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) I XAML-format med fasta sidor behöver Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer.`ResourcesFolder` låter dig ange var bilderna ska sparas och[`ResourcesFolderAlias`](../resourcesfolderalias/) låter dig ange hur bildens URI:er ska konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words som standard -bilderna i samma mapp där dokumentfilen är sparad.`ResourcesFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström har Aspose.Words ingen mapp där bilderna ska sparas, men behöver fortfarande spara bilderna någonstans. I det här fallet måste du ange en tillgänglig mapp med hjälp av`ResourcesFolder` egendom

## Exempel

Visar hur man skriver ut URI:erna för länkade resurser som skapats vid konvertering av ett dokument till .xaml i fast format.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Skapa ett "XamlFixedSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur vi sparar dokumentet till XAML-formatet.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Använd egenskapen "ResourcesFolder" för att tilldela en mapp i det lokala filsystemet till vilken
    // Aspose.Words sparar alla dokumentets länkade resurser, såsom bilder och typsnitt.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Använd egenskapen "ResourcesFolderAlias" för att använda den här mappen
    // när man konstruerar bild-URI:er istället för resursmappens namn.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // En mapp som anges av "ResourcesFolderAlias" måste innehålla resurserna istället för "ResourcesFolder".
    // Vi måste säkerställa att mappen finns innan återanropets strömmar kan lägga sina resurser i den.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Räknar och skriver ut URI:er för resurser som skapats under konvertering till fast .xaml.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // Om vi angav ett alias för resursmapp skulle vi också behöva
        // för att omdirigera varje ström för att placera dess resurs i alias-mappen.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Se även

* class [XamlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
