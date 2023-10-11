---
title: XamlFixedSaveOptions.ResourcesFolderAlias
second_title: Aspose.Words für .NET-API-Referenz
description: XamlFixedSaveOptions eigendom. Gibt den Namen des Ordners an der zum Erstellen von BildURIs verwendet wird die in ein XAMLDokument mit fester Seite geschrieben werden. Der Standardwert istNull .
type: docs
weight: 40
url: /de/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/
---
## XamlFixedSaveOptions.ResourcesFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein XAML-Dokument mit fester Seite geschrieben werden. Der Standardwert ist`Null` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

### Bemerkungen

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) Im XAML-Format mit fester Seite muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.[`ResourcesFolder`](../resourcesfolder/) Mit können Sie angeben, wo die Bilder gespeichert werden`ResourcesFolderAlias` ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

### Beispiele

Zeigt, wie die URIs verknüpfter Ressourcen gedruckt werden, die beim Konvertieren eines Dokuments in eine .xaml-Festform erstellt wurden.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Erstellen Sie ein „XamlFixedSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument im XAML-Speicherformat speichern.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Mit der Eigenschaft „ResourcesFolder“ einen Ordner im lokalen Dateisystem zuweisen, in den
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
/// Zählt und druckt URIs von Ressourcen, die während der Konvertierung in feste .xaml erstellt wurden.
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

        // Wenn wir einen Ressourcenordner-Alias angeben würden, würden wir auch Folgendes benötigen
        // um jeden Stream umzuleiten, um seine Ressource im Alias-Ordner abzulegen.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Siehe auch

* class [XamlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../xamlfixedsaveoptions/)
* Montage [Aspose.Words](../../../)


