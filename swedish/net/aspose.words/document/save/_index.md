---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words för .NET
description: Spara dina dokument enkelt med vår smarta sparmetod, som automatiskt väljer rätt format baserat på filändelsen för smidig lagring.
type: docs
weight: 750
url: /sv/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

Sparar dokumentet till en fil. Bestämmer automatiskt sparformatet från filändelsen.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på dokumentet. Om ett dokument med det angivna filnamnet redan finns, skrivs det befintliga dokumentet över. |

### Returvärde

Ytterligare information som du valfritt kan använda.

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

### Se även

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*string, [SaveFormat](../../saveformat/)*) {#save_3}

Sparar dokumentet till en fil i det angivna formatet.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på dokumentet. Om ett dokument med det angivna filnamnet redan finns, skrivs det befintliga dokumentet över. |
| saveFormat | SaveFormat | Formatet som dokumentet ska sparas i. |

### Returvärde

Ytterligare information som du valfritt kan använda.

## Exempel

Visar hur man konverterar från DOCX till HTML-format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Se även

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_4}

Sparar dokumentet till en fil med de angivna sparalternativen.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på dokumentet. Om ett dokument med det angivna filnamnet redan finns, skrivs det befintliga dokumentet över. |
| saveOptions | SaveOptions | Anger alternativen som styr hur dokumentet sparas. Kan vara`null`. |

### Returvärde

Ytterligare information som du valfritt kan använda.

## Exempel

Visar hur man förbättrar kvaliteten på ett renderat dokument med SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

Visar hur man konverterar en PDF till en .docx-fil och anpassar sparprocessen med ett SaveOptions-objekt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Ladda PDF-dokumentet som vi just sparade och konvertera det till .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// Ange egenskapen "Lösenord" för att kryptera det sparade dokumentet med ett lösenord.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

Visar hur man renderar varje sida i ett dokument till en separat TIFF-bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Ställ in egenskapen "PageSet" till numret på den första sidan från
    // vilken dokumentet ska börja renderas från.
    options.PageSet = new PageSet(i);
    // Exportera sidan med 2325x5325 pixlar och 600 dpi.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Visar hur man renderar en sida från ett dokument till en JPEG-bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Ställ in "PageSet" till "1" för att välja den andra sidan via
// det nollbaserade indexet att börja rendera dokumentet från.
options.PageSet = new PageSet(1);

// När vi sparar dokumentet i JPEG-format renderar Aspose.Words bara en sida.
// Den här bilden kommer att innehålla en sida med början från sida två,
// vilket bara kommer att vara den andra sidan i originaldokumentet.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Visar hur man konfigurerar komprimering när man sparar ett dokument som JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Sätt egenskapen "JpegQuality" till "10" för att använda starkare komprimering vid rendering av dokumentet.
// Detta minskar dokumentets filstorlek, men bilden kommer att visa mer framträdande komprimeringsartefakter.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Sätt egenskapen "JpegQuality" till "100" för att använda svagare komprimering vid rendering av dokumentet.
// Detta kommer att förbättra bildens kvalitet till bekostnad av en ökad filstorlek.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

Visar hur man konverterar ett helt dokument till PDF med tre nivåer i dokumentdispositionen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker för nivå 1 till 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Det utgående PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Om du klickar på en post i den här dispositionen kommer vi till platsen för respektive rubrik.
// Sätt egenskapen "HeadingsOutlineLevels" till "4" för att exkludera alla rubriker vars nivåer är över 4 från dispositionen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Om en dispositionspost har efterföljande poster på en högre nivå mellan sig själv och nästa post på samma eller lägre nivå,
// en pil visas till vänster om posten. Denna post är "ägare" till flera sådana "underposter".
// I vårt dokument är dispositionsposterna från den 5:e rubriknivån underposter till den andra dispositionsposten på den 4:e nivån,
// posterna på rubriknivå 4 och 5 är underposter till den andra posten på nivå 3, och så vidare.
// I dispositionen kan vi klicka på pilen för posten "ägare" för att minimera/expandera alla dess underposter.
// Sätt egenskapen "ExpandedOutlineLevels" till "2" för att automatiskt expandera alla rubriknivå 2 och lägre dispositionsposter
// och komprimerar alla poster på nivå 3 och högre när vi öppnar dokumentet.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Se även

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*Stream, [SaveFormat](../../saveformat/)*) {#save}

Sparar dokumentet till en ström med det angivna formatet.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömma var dokumentet ska sparas. |
| saveFormat | SaveFormat | Formatet som dokumentet ska sparas i. |

### Returvärde

Ytterligare information som du valfritt kan använda.

## Exempel

Visar hur man sparar ett dokument i en ström.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Verifiera att strömmen innehåller dokumentet.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Visar hur man sparar ett dokument till en bild via en ström och sedan läser bilden från den strömmen.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET461_OR_GREATER || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // Läs tillbaka strömmen till en bild.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                SKCodec codec = SKCodec.Create(stream);
                Assert.AreEqual(SKEncodedImageFormat.Bmp, codec.EncodedFormat);

                stream.Position = 0;

                using (SKBitmap image = SKBitmap.Decode(stream))
                {
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#endif
```

### Se även

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_1}

Sparar dokumentet till en ström med de angivna sparalternativen.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömma var dokumentet ska sparas. |
| saveOptions | SaveOptions | Anger alternativen som styr hur dokumentet sparas. Kan vara`null` . Om detta är`null`, kommer dokumentet att sparas i det binära DOC-formatet. |

### Returvärde

Ytterligare information som du valfritt kan använda.

## Exempel

Visar hur man konverterar endast vissa sidor i ett dokument till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur den metoden konverterar dokumentet till .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Sätt "PageIndex" till "1" för att rendera en del av dokumentet med början från den andra sidan.
    options.PageSet = new PageSet(1);

    // Detta dokument kommer att innehålla en sida med början från sida två, som bara kommer att innehålla den andra sidan.
    doc.Save(stream, options);
}
```

### Se även

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*HttpResponse, string, [ContentDisposition](../../contentdisposition/), [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_5}

Skickar dokumentet till klientens webbläsare.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| response | HttpResponse | Svarsobjekt var dokumentet ska sparas. |
| fileName | String | Namnet på dokumentet som ska visas i klientens webbläsare. Namnet får inte innehålla sökvägen. |
| contentDisposition | ContentDisposition | En[`ContentDisposition`](../../contentdisposition/) värdet that anger hur dokumentet presenteras i klientens webbläsare. |
| saveOptions | SaveOptions | Anger alternativen som styr hur dokumentet sparas. Kan vara`null`. |

### Returvärde

Ytterligare information som du valfritt kan använda.

## Anmärkningar

Internt sparar den här metoden först till en minnesström och kopierar sedan till svarsströmmen stream eftersom svarsströmmen inte stöder sökning.

## Exempel

Visar hur man utför en dokumentkoppling och sedan sparar dokumentet i klientens webbläsare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Skicka dokumentet till klientens webbläsare.
//Kastas eftersom HttpResponse är null i testet.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Vi måste stänga detta svar manuellt för att säkerställa att vi inte lägger till något överflödigt innehåll i dokumentet efter att det har sparats.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Se även

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
