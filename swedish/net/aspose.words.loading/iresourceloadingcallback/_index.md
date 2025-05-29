---
title: IResourceLoadingCallback Interface
linktitle: IResourceLoadingCallback
articleTitle: IResourceLoadingCallback
second_title: Aspose.Words för .NET
description: Styr inläsning av externa resurser i Aspose.Words med IResourceLoadingCallback-gränssnittet. Förbättra dokumentimport och bildinsättning sömlöst.
type: docs
weight: 4090
url: /sv/net/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface

Implementera detta gränssnitt om du vill styra hur Aspose.Words laddar externa resurser när importerar ett dokument och infogar bilder med hjälp av[`DocumentBuilder`](../../aspose.words/documentbuilder/) .

```csharp
public interface IResourceLoadingCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ResourceLoading](../../aspose.words.loading/iresourceloadingcallback/resourceloading/)(*[ResourceLoadingArgs](../resourceloadingargs/)*) | Anropas när Aspose.Words laddar en extern resurs. |

## Exempel

Visar hur man anpassar processen för att ladda externa resurser i ett dokument.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bilder infogas vanligtvis med hjälp av en URI, eller en byte-array.
    // Varje instans av en resursbelastning anropar vår återanropsmetod ResourceLoading.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Låter oss ladda bilder i ett dokument med hjälp av fördefinierade förkortningar, till skillnad från URI:er.
/// Detta kommer att separera bildinläsningslogiken från resten av dokumentkonstruktionen.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Om denna återanropning stöter på en av bildförkortningarna när en bild laddas,
        // den kommer att tillämpa unik logik för varje definierad förkortning istället för att behandla den som en URI.
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

### Se även

* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)
