---
title: XamlFixedSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumentexporte mit dem ResourceSavingCallback XamlFixedSaveOptions. Steuern Sie die Bild- und Schriftartenspeicherung für eine verbesserte XAML-Formateffizienz.
type: docs
weight: 20
url: /de/net/aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/
---
## XamlFixedSaveOptions.ResourceSavingCallback property

Ermöglicht die Steuerung, wie Ressourcen (Bilder und Schriftarten) gespeichert werden, wenn ein Dokument in das XAML-Format mit festen Seiten exportiert wird.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

## Beispiele

Zeigt, wie die URIs verknüpfter Ressourcen gedruckt werden, die beim Konvertieren eines Dokuments in eine XAML-Datei mit fester Form erstellt wurden.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Erstellen Sie ein "XamlFixedSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument im XAML-Speicherformat speichern.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Über die Eigenschaft „ResourcesFolder“ wird ein Ordner im lokalen Dateisystem zugewiesen, in den
    // Aspose.Words speichert alle verknüpften Ressourcen des Dokuments, wie Bilder und Schriftarten.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Verwenden Sie die Eigenschaft „ResourcesFolderAlias“, um diesen Ordner zu verwenden
    // beim Erstellen von Bild-URIs anstelle des Namens des Ressourcenordners.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Ein durch „ResourcesFolderAlias“ angegebener Ordner muss die Ressourcen anstelle von „ResourcesFolder“ enthalten.
    // Wir müssen sicherstellen, dass der Ordner vorhanden ist, bevor die Streams des Rückrufs ihre Ressourcen darin ablegen können.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Zählt und druckt URIs von Ressourcen, die während der Konvertierung in festes .xaml erstellt wurden.
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

        // Wenn wir einen Ressourcenordner-Alias angeben würden, bräuchten wir auch
        // um jeden Stream umzuleiten, um seine Ressource im Alias-Ordner abzulegen.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Siehe auch

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [XamlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
