---
title: Document.Save
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Speichert das Dokument in einer Datei. Ermittelt automatisch das Speicherformat aus der Erweiterung.
type: docs
weight: 680
url: /de/net/aspose.words/document/save/
---
## Save(string) {#save_2}

Speichert das Dokument in einer Datei. Ermittelt automatisch das Speicherformat aus der Erweiterung.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name für das Dokument. Wenn bereits ein Dokument mit dem angegebenen Dateinamen vorhanden ist, wird das vorhandene Dokument überschrieben. |

### Rückgabewert

Zusätzliche Informationen, die Sie optional verwenden können.

### Beispiele

Zeigt, wie ein Dokument geöffnet und in .PDF konvertiert wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Zeigt, wie man eine PDF-Datei in eine .docx-Datei konvertiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Laden Sie das gerade gespeicherte PDF-Dokument und konvertieren Sie es in .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

### Siehe auch

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Save(string, SaveFormat) {#save_3}

Speichert das Dokument in einer Datei im angegebenen Format.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name für das Dokument. Wenn bereits ein Dokument mit dem angegebenen Dateinamen vorhanden ist, wird das vorhandene Dokument überschrieben. |
| saveFormat | SaveFormat | Das Format, in dem das Dokument gespeichert werden soll. |

### Rückgabewert

Zusätzliche Informationen, die Sie optional verwenden können.

### Beispiele

Zeigt, wie Sie vom DOCX- in das HTML-Format konvertieren.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Siehe auch

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Save(string, SaveOptions) {#save_4}

Speichert das Dokument unter Verwendung der angegebenen Speicheroptionen in einer Datei.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name für das Dokument. Wenn bereits ein Dokument mit dem angegebenen Dateinamen vorhanden ist, wird das vorhandene Dokument überschrieben. |
| saveOptions | SaveOptions | Gibt die Optionen an, die steuern, wie das Dokument gespeichert wird. Kann null sein. |

### Rückgabewert

Zusätzliche Informationen, die Sie optional verwenden können.

### Beispiele

Zeigt, wie die Qualität eines gerenderten Dokuments mit SaveOptions verbessert wird.

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

Zeigt, wie Sie eine PDF-Datei in eine .docx-Datei konvertieren und den Speichervorgang mit einem SaveOptions-Objekt anpassen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Laden Sie das gerade gespeicherte PDF-Dokument und konvertieren Sie es in .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// Legen Sie die Eigenschaft "Password" fest, um das gespeicherte Dokument mit einem Passwort zu verschlüsseln.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

Zeigt, wie jede Seite eines Dokuments in ein separates TIFF-Bild gerendert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild rendert.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Setzen Sie die Eigenschaft "PageSet" auf die Nummer der ersten Seite von
    // von wo aus das Dokument gerendert werden soll.
    options.PageSet = new PageSet(i);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Zeigt, wie eine Seite aus einem Dokument in ein JPEG-Bild gerendert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild rendert.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// Setzen Sie "PageSet" auf "1", um die zweite Seite über auszuwählen
// der nullbasierte Index, von dem aus das Dokument gerendert werden soll.
options.PageSet = new PageSet(1);

// Wenn wir das Dokument im JPEG-Format speichern, rendert Aspose.Words nur eine Seite.
// Dieses Bild enthält eine Seite beginnend mit Seite zwei,
// das wird nur die zweite Seite des Originaldokuments sein.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Zeigt, wie die Komprimierung konfiguriert wird, während ein Dokument als JPEG gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild rendert.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Setzen Sie die Eigenschaft "JpegQuality" auf "10", um beim Rendern des Dokuments eine stärkere Komprimierung zu verwenden.
// Dadurch wird die Dateigröße des Dokuments reduziert, aber das Bild zeigt deutlichere Komprimierungsartefakte.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Legen Sie die Eigenschaft "JpegQuality" auf "100" fest, um beim Rendern des Dokuments eine schwächere Komprimierung zu verwenden.
// Dadurch wird die Bildqualität auf Kosten einer erhöhten Dateigröße verbessert.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Zeigt, wie ein ganzes Dokument mit drei Ebenen in der Dokumentgliederung in PDF konvertiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Überschriften der Ebenen 1 bis 5 einfügen.
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

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Das ausgegebene PDF-Dokument enthält eine Gliederung, die ein Inhaltsverzeichnis ist, das Überschriften im Dokumentkörper auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "4", um alle Überschriften, deren Ebenen höher als 4 sind, von der Gliederung auszuschließen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Wenn ein Gliederungseintrag nachfolgende Einträge einer höheren Ebene zwischen sich und dem nächsten Eintrag der gleichen oder niedrigeren Ebene hat,
// Links neben dem Eintrag erscheint ein Pfeil. Dieser Eintrag ist der "Eigentümer" mehrerer solcher "Untereinträge".
// In unserem Dokument sind die Gliederungseinträge der 5. Überschriftenebene Untereinträge der zweiten Gliederungsebene der 4. Ebene,
 // Die Einträge der 4. und 5. Überschriftenebene sind Untereinträge des zweiten Eintrags der 3. Ebene und so weiter.
// In der Gliederung können wir auf den Pfeil des „Besitzer“-Eintrags klicken, um alle seine Untereinträge zu reduzieren/erweitern.
// Legen Sie die Eigenschaft "ExpandedOutlineLevels" auf "2" fest, um automatisch alle Einträge der Überschriftenebene 2 und der unteren Gliederung zu erweitern
 // und alle Einträge der Ebene und 3 und höher reduzieren, wenn wir das Dokument öffnen.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Siehe auch

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Save(Stream, SaveFormat) {#save}

Speichert das Dokument unter Verwendung des angegebenen Formats in einem Stream.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Streamen Sie, wo das Dokument gespeichert werden soll. |
| saveFormat | SaveFormat | Das Format, in dem das Dokument gespeichert werden soll. |

### Rückgabewert

Zusätzliche Informationen, die Sie optional verwenden können.

### Beispiele

Zeigt, wie ein Dokument in einem Stream gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Prüfen, ob der Stream das Dokument enthält.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Zeigt, wie Sie ein Dokument per Stream in einem Bild speichern und dann das Bild aus diesem Stream lesen.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET48 || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // Lies den Stream zurück in ein Bild.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER || __MOBILE__
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

### Siehe auch

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Save(Stream, SaveOptions) {#save_1}

Speichert das Dokument unter Verwendung der angegebenen Speicheroptionen in einem Stream.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Streamen Sie, wo das Dokument gespeichert werden soll. |
| saveOptions | SaveOptions | Gibt die Optionen an, die steuern, wie das Dokument gespeichert wird. Kann null sein. Wenn dies null ist, wird das Dokument im binären DOC-Format gespeichert. |

### Rückgabewert

Zusätzliche Informationen, die Sie optional verwenden können.

### Beispiele

Zeigt, wie nur einige der Seiten in einem Dokument in PDF konvertiert werden.

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
    // Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
    PdfSaveOptions options = new PdfSaveOptions();

    // "PageIndex" auf "1" setzen, um einen Teil des Dokuments ab der zweiten Seite zu rendern.
    options.PageSet = new PageSet(1);

    // Dieses Dokument enthält eine Seite beginnend mit Seite zwei, die nur die zweite Seite enthält.
    doc.Save(stream, options);
}
```

### Siehe auch

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Save(HttpResponse, string, ContentDisposition, SaveOptions) {#save_5}

Sendet das Dokument an den Client-Browser.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| response | HttpResponse | Antwortobjekt, in dem das Dokument gespeichert werden soll. |
| fileName | String | Der Name für das Dokument, das im Client-Browser angezeigt wird. Der Name sollte keinen Pfad enthalten. |
| contentDisposition | ContentDisposition | EIN[`ContentDisposition`](../../contentdisposition/) Der Wert that gibt an, wie das Dokument im Client-Browser dargestellt wird. |
| saveOptions | SaveOptions | Gibt die Optionen an, die steuern, wie das Dokument gespeichert wird. Kann null sein. |

### Rückgabewert

Zusätzliche Informationen, die Sie optional verwenden können.

### Bemerkungen

Intern speichert diese Methode zuerst in einem Speicherstrom und kopiert dann in den Antwortstrom stream , da der Antwortstrom die Suche nicht unterstützt.

### Beispiele

Zeigt, wie Sie einen Seriendruck durchführen und das Dokument dann im Client-Browser speichern.

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

// Senden Sie das Dokument an den Client-Browser.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Wird ausgelöst, weil HttpResponse im Test null ist.

// Wir müssen diese Antwort manuell schließen, um sicherzustellen, dass wir dem Dokument nach dem Speichern keine überflüssigen Inhalte hinzufügen.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Siehe auch

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


