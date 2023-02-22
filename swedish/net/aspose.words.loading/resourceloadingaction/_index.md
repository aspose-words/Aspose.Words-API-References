---
title: Enum ResourceLoadingAction
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Loading.ResourceLoadingAction uppräkning. Anger läget för resursladdning.
type: docs
weight: 3480
url: /sv/net/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enumeration

Anger läget för resursladdning.

```csharp
public enum ResourceLoadingAction
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Default | `0` | Aspose.Words laddar den här resursen som vanligt. |
| Skip | `1` | Aspose.Words hoppar över laddningen av denna resurs. Endast länk utan data kommer att lagras för en bild, CSS-formatmall kommer att ignoreras för HTML-format. |
| UserProvided | `2` | Aspose.Words kommer att använda byte-array som tillhandahålls av användaren i[`SetData`](../resourceloadingargs/setdata/) som resursdata. |

### Exempel

Visar hur man anpassar processen för att ladda externa resurser i ett dokument.

```csharp
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bilder infogas vanligtvis med en URI eller en byte-array.
    // Varje instans av en resursladdning kommer att anropa vår callbacks ResourceLoading-metod.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");

/// <summary>
/// Låter oss läsa in bilder i ett dokument med fördefinierade förkortningar, till skillnad från URI:er.
/// Detta kommer att separera logik för bildladdning från resten av dokumentkonstruktionen.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Om denna återuppringning stöter på en av bildens förkortningar när en bild laddas,
        // det kommer att tillämpa unik logik för varje definierad stenografi istället för att behandla den som en URI.
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


