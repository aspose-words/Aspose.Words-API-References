---
title: ResourceLoadingArgs.SetData
linktitle: SetData
articleTitle: SetData
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ResourceLoadingArgs SetData-Methode das Benutzererlebnis verbessert, indem sie Ressourcendaten effizient verwaltet, um eine optimale Leistung zu erzielen.
type: docs
weight: 40
url: /de/net/aspose.words.loading/resourceloadingargs/setdata/
---
## ResourceLoadingArgs.SetData method

Setzt benutzerdefinierte Daten der Ressource, die verwendet wird wenn[`ResourceLoading`](../../iresourceloadingcallback/resourceloading/) gibt zurückUserProvided .

```csharp
public void SetData(byte[] data)
```

## Beispiele

Zeigt, wie der Prozess des Ladens externer Ressourcen in ein Dokument angepasst wird.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bilder werden normalerweise mithilfe einer URI oder eines Byte-Arrays eingefügt.
    // Jede Instanz einer Ressourcenladung ruft die ResourceLoading-Methode unseres Rückrufs auf.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Ermöglicht uns, Bilder mithilfe vordefinierter Abkürzungen statt URIs in ein Dokument zu laden.
/// Dadurch wird die Bildladelogik vom Rest der Dokumentkonstruktion getrennt.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Wenn dieser Rückruf beim Laden eines Bildes auf eine der Bildkürzel stößt,
        // Es wird für jede definierte Abkürzung eine eindeutige Logik angewendet, anstatt sie als URI zu behandeln.
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

* class [ResourceLoadingArgs](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
