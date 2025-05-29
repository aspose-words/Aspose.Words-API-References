---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words för .NET
description: Skapa enkelt tomma Word-dokument med vår användarvänliga dokumentkonstruktör. Effektivisera din skrivprocess idag!
type: docs
weight: 10
url: /sv/net/aspose.words/document/document/
---
## Document() {#constructor}

Skapar ett tomt Word-dokument.

```csharp
public Document()
```

## Anmärkningar

Ett tomt dokument hämtas från resurser, och som standard ser det resulterande dokumentet mer ut som skapat avWord2007. Detta tomma dokument innehåller en tabell över standardteckensnitt, minimala standardstilar och latenta stilar.

[`OptimizeFor`](../../../aspose.words.settings/compatibilityoptions/optimizefor/) Metoden kan användas för att optimera dokumentinnehållet samt standardbeteendet för Aspose.Words för en viss version av MS Word.

Dokumentets pappersstorlek är som standard Letter. Om du vill ändra utskriftsformatet använder du [`PageSetup`](../../section/pagesetup/).

Efter skapandet kan du använda[`DocumentBuilder`](../../documentbuilder/) för att enkelt lägga till dokumentinnehåll.

## Exempel

Visar hur man formaterar en textsekvens med hjälp av dess font-egenskap.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Visar hur man skapar ett enkelt dokument.

```csharp
Document doc = new Document();

// Nya dokumentobjekt levereras som standard med den minimala uppsättningen noder
// krävs för att börja lägga till innehåll som text och former: ett avsnitt, en brödtext och ett stycke.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

Visar hur man skapar och laddar dokument.

```csharp
// Det finns två sätt att skapa ett Document-objekt med hjälp av Aspose.Words.
// 1 - Skapa ett tomt dokument:
Document doc = new Document();

// Nya dokumentobjekt levereras som standard med den minimala uppsättningen noder
// krävs för att börja lägga till innehåll som text och former: ett avsnitt, en brödtext och ett stycke.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Ladda ett dokument som finns i det lokala filsystemet:
doc = new Document(MyDir + "Document.docx");

// Inlästa dokument kommer att ha innehåll som vi kan komma åt och redigera.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Vissa operationer som måste utföras under laddning, till exempel att använda ett lösenord för att dekryptera ett dokument,
// kan göras genom att skicka ett LoadOptions-objekt när dokumentet laddas.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

Öppnar ett befintligt dokument från en fil. Identifierar automatiskt filformatet.

```csharp
public Document(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filnamnet på dokumentet som ska öppnas. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception/) | Dokumentet verkar vara skadat och kan inte läsas in. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklarna. |
| IOException | Det finns ett indata/utdata-undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du angav ett felaktigt lösenord. |
| ArgumentException | Filnamnet får inte vara null eller en tom sträng. |

## Exempel

Visar hur man öppnar ett dokument och konverterar det till .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Visar hur man konverterar en PDF till en .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Ladda PDF-dokumentet som vi just sparade och konvertera det till .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Visar hur man laddar en PDF.

```csharp
Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// Nedan följer två sätt att ladda PDF-dokument med Aspose-produkter.
// 1 - Ladda som ett Aspose.Words-dokument:
Document asposeWordsDoc = new Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Ladda som ett Aspose.Pdf-dokument:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

Öppnar ett befintligt dokument från en fil. Gör det möjligt att ange ytterligare alternativ, till exempel ett krypteringslösenord.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filnamnet på dokumentet som ska öppnas. |
| loadOptions | LoadOptions | Ytterligare alternativ att använda när du laddar ett dokument. Kan vara`null`. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception/) | Dokumentet verkar vara skadat och kan inte läsas in. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklarna. |
| IOException | Det finns ett indata/utdata-undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du angav ett felaktigt lösenord. |
| ArgumentException | Filnamnet får inte vara null eller en tom sträng. |

## Exempel

Visar hur man laddar ett krypterat Microsoft Word-dokument.

```csharp
Document doc;

// Aspose.Words utlöser ett undantag om vi försöker öppna ett krypterat dokument utan dess lösenord.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// När ett sådant dokument laddas skickas lösenordet till dokumentets konstruktor med hjälp av ett LoadOptions-objekt.
LoadOptions options = new LoadOptions("docPassword");

// Det finns två sätt att läsa in ett krypterat dokument med ett LoadOptions-objekt.
// 1 - Ladda dokumentet från det lokala filsystemet med filnamn:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Ladda dokumentet från en ström:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Visar hur man skapar och laddar dokument.

```csharp
// Det finns två sätt att skapa ett Document-objekt med hjälp av Aspose.Words.
// 1 - Skapa ett tomt dokument:
Document doc = new Document();

// Nya dokumentobjekt levereras som standard med den minimala uppsättningen noder
// krävs för att börja lägga till innehåll som text och former: ett avsnitt, en brödtext och ett stycke.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Ladda ett dokument som finns i det lokala filsystemet:
doc = new Document(MyDir + "Document.docx");

// Inlästa dokument kommer att ha innehåll som vi kan komma åt och redigera.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Vissa operationer som måste utföras under laddning, till exempel att använda ett lösenord för att dekryptera ett dokument,
// kan göras genom att skicka ett LoadOptions-objekt när dokumentet laddas.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Se även

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

Öppnar ett befintligt dokument från en ström. Identifierar automatiskt filformatet.

```csharp
public Document(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömma varifrån dokumentet ska laddas. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception/) | Dokumentet verkar vara skadat och kan inte läsas in. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklarna. |
| IOException | Det finns ett indata/utdata-undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du angav ett felaktigt lösenord. |
| ArgumentNullException | Strömmen kan inte vara null. |
| NotSupportedException | Strömmen stöder inte läsning eller sökning. |
| ObjectDisposedException | Strömmen är ett avfallsobjekt. |

## Anmärkningar

Dokumentet måste lagras i början av strömmen. Strömmen måste stödja slumpmässig positionering.

## Exempel

Visar hur man laddar ett dokument med hjälp av en ström.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Visar hur man laddar ett dokument från en URL.

```csharp
// Skapa en URL som pekar till ett Microsoft Word-dokument.
const string url = "https://filesamples.com/samples/document/docx/sample3.docx";

// Ladda ner dokumentet till en byte-array och ladda sedan den arrayen till ett dokument med hjälp av en minnesström.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // I det här skedet kan vi läsa och redigera dokumentets innehåll och sedan spara det i det lokala filsystemet.
        Assert.AreEqual("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
                        "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
                        "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.",
            doc.FirstSection.Body.Paragraphs[3].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

Öppnar ett befintligt dokument från en ström. Gör det möjligt att ange ytterligare alternativ, till exempel ett krypteringslösenord.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen varifrån dokumentet ska läsas in. |
| loadOptions | LoadOptions | Ytterligare alternativ att använda när du laddar ett dokument. Kan vara`null`. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception/) | Dokumentet verkar vara skadat och kan inte läsas in. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklarna. |
| IOException | Det finns ett indata/utdata-undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du angav ett felaktigt lösenord. |
| ArgumentNullException | Strömmen kan inte vara null. |
| NotSupportedException | Strömmen stöder inte läsning eller sökning. |
| ObjectDisposedException | Strömmen är ett avfallsobjekt. |

## Anmärkningar

Dokumentet måste lagras i början av strömmen. Strömmen måste stödja slumpmässig positionering.

## Exempel

Visar hur man öppnar ett HTML-dokument med bilder från en ström med hjälp av en bas-URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Skicka URI:n för basmappen när den laddas
    // så att alla bilder med relativa URI:er i HTML-dokumentet kan hittas.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifiera att dokumentets första form innehåller en giltig bild.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

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

Visar hur man laddar ett krypterat Microsoft Word-dokument.

```csharp
Document doc;

// Aspose.Words utlöser ett undantag om vi försöker öppna ett krypterat dokument utan dess lösenord.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// När ett sådant dokument laddas skickas lösenordet till dokumentets konstruktor med hjälp av ett LoadOptions-objekt.
LoadOptions options = new LoadOptions("docPassword");

// Det finns två sätt att läsa in ett krypterat dokument med ett LoadOptions-objekt.
// 1 - Ladda dokumentet från det lokala filsystemet med filnamn:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Ladda dokumentet från en ström:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Se även

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
