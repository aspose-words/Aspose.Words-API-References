---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words för .NET
description: Upptäck enum-filen Aspose.Words.LoadFormat, som definierar dokumentformat för sömlös inläsning och förbättrad kompatibilitet i dina applikationer.
type: docs
weight: 4000
url: /sv/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Anger formatet på dokumentet som ska läsas in.

```csharp
public enum LoadFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Instruerar Aspose.Words att automatiskt känna igen formatet. |
| MsWorks | `8` | Microsoft Works 8-dokument. |
| Doc | `10` | Microsoft Word 95- eller Word 97-2003-dokument. |
| Dot | `11` | Mall för Microsoft Word 95 eller Word 97 - 2003. |
| DocPreWord60 | `12` | Dokumentet är i formatet före Word 95. Aspose.Words stöder för närvarande inte laddning av sådana dokument. |
| Docx | `20` | Office Open XML WordprocessingML-dokument (makrofritt). |
| Docm | `21` | Office Open XML WordprocessingML Makroaktiverat dokument. |
| Dotx | `22` | Office Open XML WordprocessingML-mall (makrofri). |
| Dotm | `23` | Office Open XML WordprocessingML Makroaktiverad mall. |
| FlatOpc | `24` | Office Open XML WordprocessingML lagras i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML Makroaktiverat dokument lagrat i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplate | `26` | Office Open XML WordprocessingML-mall (makrofri) lagrad i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplateMacroEnabled | `27` | Office Open XML WordprocessingML Makroaktiverad mall lagrad i en platt XML-fil istället för ett ZIP-paket. |
| Rtf | `30` | RTF-format. |
| WordML | `31` | Microsoft Word 2003 WordprocessingML-format. |
| Html | `50` | HTML-format. |
| Mhtml | `51` | MHTML-format (webbarkiv). |
| Mobi | `52` | MOBI-format. Används av MobiPocket-läsare och Amazon Kindle-läsare. |
| Chm | `53` | CHM-format (kompilerad HTML-hjälp). |
| Azw3 | `54` | AZW3-format. Används av Amazon Kindle-läsare. |
| Epub | `55` | EPUB-format. |
| Odt | `60` | ODF-textdokument. |
| Ott | `61` | ODF-textdokumentmall. |
| Text | `62` | Vanlig text. |
| Markdown | `63` | Markdown-textdokument. |
| Pdf | `64` | Pdf-dokument. |
| Xml | `65` | XML-dokument. |
| Unknown | `255` | Okänt format, kan inte laddas av Aspose.Words. |

## Exempel

Visar hur man sparar en webbsida som en .docx-fil.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL:en används återigen som en baseUri för att säkerställa att alla relativa bildsökvägar hämtas korrekt.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Ladda HTML-dokumentet från strömmen och skicka LoadOptions-objektet.
        Document doc = new Document(stream, options);

        // I det här skedet kan vi läsa och redigera dokumentets innehåll och sedan spara det i det lokala filsystemet.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Visar hur man anger en bas-URI när man öppnar ett HTML-dokument.

```csharp
// Anta att vi vill ladda ett .html-dokument som innehåller en bild länkad av en relativ URI
// medan bilden är på en annan plats. I så fall måste vi omvandla den relativa URI:n till en absolut.
 // Vi kan tillhandahålla en bas-URI med hjälp av ett HtmlLoadOptions-objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Även om bilden i indata-.html-filen var trasig, hjälpte vår anpassade bas-URI oss att reparera länken.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Detta utdatadokument visar bilden som saknades.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

Visar hur man använder FileFormatUtil-metoderna för att identifiera ett dokuments format.

```csharp
// Ladda ett dokument från en fil som saknar filändelse och identifiera sedan dess filformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Nedan följer två metoder för att konvertera ett LoadFormat till motsvarande SaveFormat.
    // 1 - Hämta filändelsen för LoadFormat och hämta sedan motsvarande SaveFormat från den strängen:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertera LoadFormat direkt till dess SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Ladda ett dokument från strömmen och spara det sedan till den automatiskt upptäckta filändelsen.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
