---
title: DocumentBase.ResourceLoadingCallback
linktitle: ResourceLoadingCallback
articleTitle: ResourceLoadingCallback
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre DocumentBase mit der ResourceLoadingCallback-Eigenschaft für eine effiziente Kontrolle des Ladens externer Ressourcen. Steigern Sie noch heute die Leistung!
type: docs
weight: 80
url: /de/net/aspose.words/documentbase/resourceloadingcallback/
---
## DocumentBase.ResourceLoadingCallback property

Ermöglicht die Steuerung des Ladens externer Ressourcen.

```csharp
public IResourceLoadingCallback ResourceLoadingCallback { get; set; }
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

* interface [IResourceLoadingCallback](../../../aspose.words.loading/iresourceloadingcallback/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
