---
title: IResourceLoadingCallback Interface
linktitle: IResourceLoadingCallback
articleTitle: IResourceLoadingCallback
second_title: Aspose.Words für .NET
description: Steuern Sie das Laden externer Ressourcen in Aspose.Words mit der IResourceLoadingCallback-Schnittstelle. Optimieren Sie den Dokumentimport und das Einfügen von Bildern nahtlos.
type: docs
weight: 4090
url: /de/net/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words externe Ressourcen lädt, wenn ein Dokument importiert und Bilder eingefügt werden mit[`DocumentBuilder`](../../aspose.words/documentbuilder/) .

```csharp
public interface IResourceLoadingCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ResourceLoading](../../aspose.words.loading/iresourceloadingcallback/resourceloading/)(*[ResourceLoadingArgs](../resourceloadingargs/)*) | Wird aufgerufen, wenn Aspose.Words eine externe Ressource lädt. |

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
