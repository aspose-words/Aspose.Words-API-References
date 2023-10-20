---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: Aspose.Words für .NET
description: Aspose.Words.Loading.ResourceLoadingArgs klas. Stellt Daten für die bereitResourceLoading method in C#.
type: docs
weight: 3690
url: /de/net/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class

Stellt Daten für die bereit[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) method.

```csharp
public class ResourceLoadingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | Ursprünglicher URI der Ressource, wie im importierten Dokument angegeben. |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | Art der Ressource. |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | URI der Ressource, die zum Herunterladen von verwendet wird, wenn[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) kehrt zurückDefault. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | Legt vom Benutzer bereitgestellte Daten der Ressource fest, die verwendet wird wenn[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) kehrt zurückUserProvided . |

## Beispiele

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

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
