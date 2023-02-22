---
title: LoadOptions.LoadOptions
second_title: Aspose.Words för .NET API Referens
description: LoadOptions byggare. Initierar en ny instans av denna klass med standardvärden.
type: docs
weight: 10
url: /sv/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Initierar en ny instans av denna klass med standardvärden.

```csharp
public LoadOptions()
```

### Exempel

Visar hur man öppnar ett HTML-dokument med bilder från en ström med en bas-URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Skicka URI:n för basmappen medan du laddar den
    // så att alla bilder med relativa URI:er i HTML-dokumentet kan hittas.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifiera att den första formen av dokumentet innehåller en giltig bild.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)

---

## LoadOptions(string) {#constructor_2}

En genväg för att initiera en ny instans av denna klass med det angivna lösenordet för att ladda ett krypterat dokument.

```csharp
public LoadOptions(string password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| password | String | Lösenordet för att öppna ett krypterat dokument. Kan vara null eller tom sträng. |

### Exempel

Visar hur man laddar ett krypterat Microsoft Word-dokument.

```csharp
Document doc;

// Aspose.Words ger ett undantag om vi försöker öppna ett krypterat dokument utan dess lösenord.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// När ett sådant dokument laddas skickas lösenordet till dokumentets konstruktor med hjälp av ett LoadOptions-objekt.
LoadOptions options = new LoadOptions("docPassword");

// Det finns två sätt att ladda ett krypterat dokument med ett LoadOptions-objekt.
// 1 - Ladda dokumentet från det lokala filsystemet efter filnamn:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Ladda dokumentet från en ström:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)

---

## LoadOptions(LoadFormat, string, string) {#constructor_1}

En genväg för att initiera en ny instans av denna klass med egenskaper inställda på de angivna värdena.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| loadFormat | LoadFormat | Formatet på dokumentet som ska laddas. |
| password | String | Lösenordet för att öppna ett krypterat dokument. Kan vara null eller tom sträng. |
| baseUri | String | Strängen som kommer att användas för att lösa relativa URI:er till absoluta. Kan vara null eller tom sträng. |

### Exempel

Visar hur du sparar en webbsida som en .docx-fil.

```csharp
const string url = "http://www.aspose.com/";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // URL:en används igen som en baseUri för att säkerställa att eventuella relativa bildsökvägar hämtas korrekt.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Ladda HTML-dokumentet från stream och skicka LoadOptions-objektet.
        Document doc = new Document(stream, options);

        // I detta skede kan vi läsa och redigera dokumentets innehåll och sedan spara det i det lokala filsystemet.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Visar hur du anger en bas-URI när du öppnar ett HTML-dokument.

```csharp
// Anta att vi vill ladda ett .html-dokument som innehåller en bild länkad av en relativ URI
// medan bilden är på en annan plats. I så fall måste vi lösa den relativa URI till en absolut.
  // Vi kan tillhandahålla en bas-URI med hjälp av ett HtmlLoadOptions-objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Medan bilden var trasig i inmatningen .html, hjälpte vår anpassade bas-URI oss att reparera länken.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Detta utdatadokument visar bilden som saknades.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Se även

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)


