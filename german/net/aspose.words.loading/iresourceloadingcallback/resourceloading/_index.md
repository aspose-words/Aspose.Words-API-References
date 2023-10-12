---
title: IResourceLoadingCallback.ResourceLoading
second_title: Aspose.Words für .NET-API-Referenz
description: IResourceLoadingCallback methode. Wird aufgerufen wenn Aspose.Words eine externe Ressource lädt.
type: docs
weight: 10
url: /de/net/aspose.words.loading/iresourceloadingcallback/resourceloading/
---
## IResourceLoadingCallback.ResourceLoading method

Wird aufgerufen, wenn Aspose.Words eine externe Ressource lädt.

```csharp
public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
```

### Beispiele

Zeigt, wie Sie den Prozess des Ladens externer Ressourcen in ein Dokument anpassen.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bilder werden normalerweise über einen URI oder ein Byte-Array eingefügt.
    // Jede Instanz einer Ressourcenlast ruft die ResourceLoading-Methode unseres Rückrufs auf.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Ermöglicht das Laden von Bildern in ein Dokument mithilfe vordefinierter Abkürzungen im Gegensatz zu URIs.
/// Dadurch wird die Bildladelogik vom Rest der Dokumentkonstruktion getrennt.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Wenn dieser Rückruf beim Laden eines Bildes auf eine der Bildkürzel stößt,
        // Es wird eine eindeutige Logik für jede definierte Abkürzung angewendet, anstatt sie als URI zu behandeln.
        if (args.ResourceType == ResourceType.Image)
            switch (args.OriginalUri)
            {
                case "Google logo":
                    using (WebClient webClient = new WebClient())
                    {
                        args.SetData(webClient.DownloadData("http://www.google.com/images/logos/ps_logo2.png"));
                    }

                    return ResourceLoadingAction.UserProvided;

                case "Aspose logo":
                    args.SetData(File.ReadAllBytes(ImageDir + "Logo.jpg"));

                    return ResourceLoadingAction.UserProvided;

                case "Watermark":
                    args.SetData(File.ReadAllBytes(ImageDir + "Transparent background logo.png"));

                    return ResourceLoadingAction.UserProvided;
            }

        return ResourceLoadingAction.Default;
    }
}
```

### Siehe auch

* enum [ResourceLoadingAction](../../resourceloadingaction/)
* class [ResourceLoadingArgs](../../resourceloadingargs/)
* interface [IResourceLoadingCallback](../)
* namensraum [Aspose.Words.Loading](../../iresourceloadingcallback/)
* Montage [Aspose.Words](../../../)


