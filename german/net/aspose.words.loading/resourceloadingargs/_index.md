---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Loading.ResourceLoadingArgs, die die Effizienz beim Laden von Ressourcen in Ihren Anwendungen verbessert. Schalten Sie noch heute die nahtlose Integration frei!
type: docs
weight: 4150
url: /de/net/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class

Liefert Daten für die[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) Methode.

```csharp
public class ResourceLoadingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | Ursprünglicher URI der Ressource, wie im importierten Dokument angegeben. |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | Ressourcentyp. |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | URI der Ressource, die zum Herunterladen verwendet wird wenn[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) gibt zurückDefault. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | Setzt benutzerdefinierte Daten der Ressource, die verwendet wird wenn[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) gibt zurückUserProvided . |

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

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
