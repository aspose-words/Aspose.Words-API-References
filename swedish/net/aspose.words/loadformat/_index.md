---
title: Enum LoadFormat
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.LoadFormat uppräkning. Indikerar formatet på dokumentet som ska laddas.
type: docs
weight: 3550
url: /sv/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Indikerar formatet på dokumentet som ska laddas.

```csharp
public enum LoadFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Instruerar Aspose.Words att känna igen formatet automatiskt. |
| Doc | `10` | Microsoft Word 95 eller Word 97 - 2003 Document. |
| Dot | `11` | Microsoft Word 95 eller Word 97 - 2003 Mall. |
| DocPreWord60 | `12` | Dokumentet är i pre-Word 95-format. Aspose.Words stöder för närvarande inte inläsning av sådana dokument. |
| Docx | `20` | Office Open XML WordprocessingML-dokument (makrofritt). |
| Docm | `21` | Office Open XML WordprocessingML Macro-Enabled Document. |
| Dotx | `22` | Office Open XML WordprocessingML-mall (makrofri). |
| Dotm | `23` | Office Open XML WordprocessingML Macro-Enabled Mall. |
| FlatOpc | `24` | Office Open XML WordprocessingML lagrad i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML Macro-Enabled Document lagras i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplate | `26` | Office Open XML WordprocessingML-mall (makrofri) lagrad i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplateMacroEnabled | `27` | Office Open XML WordprocessingML Macro-Enabled Mall lagrad i en platt XML-fil istället för ett ZIP-paket. |
| Rtf | `30` | RTF-format. |
| WordML | `31` | Microsoft Word 2003 WordprocessingML-format. |
| Html | `50` | HTML-format. |
| Mhtml | `51` | MHTML (webbarkiv) format. |
| Mobi | `52` | MOBI-format. Används av MobiPocket-läsare och Amazon Kindle-läsare. |
| Chm | `53` | CHM (Compiled HTML Help) format. |
| Azw3 | `54` | AZW3-format. Används av Amazon Kindle-läsare. |
| Epub | `55` | EPUB-format. |
| Odt | `60` | ODF-textdokument. |
| Ott | `61` | ODF-textdokumentmall. |
| Text | `62` | Vanlig text. |
| Markdown | `63` | Markdown textdokument. |
| Pdf | `64` | Pdf-dokument. |
| Xml | `65` | XML-dokument. |
| Unknown | `255` | Okänt format, kan inte laddas av Aspose.Words. |

### Exempel

Visar hur du sparar en webbsida som en .docx-fil.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
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

Visar hur du använder FileFormatUtil-metoderna för att upptäcka formatet på ett dokument.

```csharp
// Ladda ett dokument från en fil som saknar filtillägg, och identifiera sedan dess filformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Nedan finns två metoder för att konvertera ett LoadFormat till dess motsvarande SaveFormat.
    // 1 - Hämta filtilläggssträngen för LoadFormat och hämta sedan motsvarande SaveFormat från den strängen:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertera LoadFormat direkt till dess SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Ladda ett dokument från strömmen och spara det sedan i det automatiskt upptäckta filtillägget.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


