---
title: XamlFixedSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words för .NET
description: Optimera dina dokumentexporter med XamlFixedSaveOptions ResourceSavingCallback. Kontrollera bild- och teckensnittssparning för förbättrad XAML-formateffektivitet.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/
---
## XamlFixedSaveOptions.ResourceSavingCallback property

Gör det möjligt att styra hur resurser (bilder och teckensnitt) sparas när ett dokument exporteras till ett fast XAML-format.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

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

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [XamlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
