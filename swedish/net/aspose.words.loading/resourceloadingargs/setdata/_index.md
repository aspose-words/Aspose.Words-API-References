---
title: ResourceLoadingArgs.SetData
linktitle: SetData
articleTitle: SetData
second_title: Aspose.Words för .NET
description: Upptäck hur metoden ResourceLoadingArgs SetData förbättrar användarupplevelsen genom att effektivt hantera resursdata för optimal prestanda.
type: docs
weight: 40
url: /sv/net/aspose.words.loading/resourceloadingargs/setdata/
---
## ResourceLoadingArgs.SetData method

Ställer in användardefinierade data för resursen som används om[`ResourceLoading`](../../iresourceloadingcallback/resourceloading/) returnerarUserProvided .

```csharp
public void SetData(byte[] data)
```

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

* class [ResourceLoadingArgs](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
