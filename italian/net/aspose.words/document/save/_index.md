---
title: Document.Save
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Salva il documento in un file. Determina automaticamente il formato di salvataggio dallestensione.
type: docs
weight: 680
url: /it/net/aspose.words/document/save/
---
## Save(string) {#save_2}

Salva il documento in un file. Determina automaticamente il formato di salvataggio dall'estensione.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome del documento. Se esiste già un documento con il nome file specificato , il documento esistente viene sovrascritto. |

### Valore di ritorno

Informazioni aggiuntive che puoi utilizzare facoltativamente.

### Esempi

Mostra come aprire un documento e convertirlo in .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Mostra come convertire un PDF in un .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Carica il documento PDF che abbiamo appena salvato e convertilo in .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

### Guarda anche

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

---

## Save(string, SaveFormat) {#save_3}

Salva il documento in un file nel formato specificato.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome del documento. Se esiste già un documento con il nome file specificato , il documento esistente viene sovrascritto. |
| saveFormat | SaveFormat | Il formato in cui salvare il documento. |

### Valore di ritorno

Informazioni aggiuntive che puoi utilizzare facoltativamente.

### Esempi

Mostra come convertire da DOCX in formato HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Guarda anche

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

---

## Save(string, SaveOptions) {#save_4}

Salva il documento in un file utilizzando le opzioni di salvataggio specificate.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome del documento. Se esiste già un documento con il nome file specificato , il documento esistente viene sovrascritto. |
| saveOptions | SaveOptions | Specifica le opzioni che controllano la modalità di salvataggio del documento. Può essere nullo. |

### Valore di ritorno

Informazioni aggiuntive che puoi utilizzare facoltativamente.

### Esempi

Mostra come migliorare la qualità di un documento sottoposto a rendering con SaveOptions.

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

Mostra come convertire un PDF in un .docx e personalizzare il processo di salvataggio con un oggetto SaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Carica il documento PDF che abbiamo appena salvato e convertilo in .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// Imposta la proprietà "Password" per crittografare il documento salvato con una password.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

Mostra come eseguire il rendering di ogni pagina di un documento in un'immagine TIFF separata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Imposta la proprietà "PageSet" sul numero della prima pagina da
    // da cui iniziare il rendering del documento.
    options.PageSet = new PageSet(i);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Mostra come eseguire il rendering di una pagina da un documento a un'immagine JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// Imposta "PageSet" su "1" per selezionare la seconda pagina tramite
// l'indice in base zero da cui iniziare il rendering del documento.
options.PageSet = new PageSet(1);

// Quando salviamo il documento nel formato JPEG, Aspose.Words esegue il rendering di una sola pagina.
// Questa immagine conterrà una pagina a partire dalla seconda pagina,
// che sarà solo la seconda pagina del documento originale.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Mostra come configurare la compressione durante il salvataggio di un documento come JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Imposta la proprietà "JpegQuality" su "10" per utilizzare una compressione più forte durante il rendering del documento.
// Ciò ridurrà le dimensioni del file del documento, ma l'immagine mostrerà artefatti di compressione più evidenti.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Imposta la proprietà "JpegQuality" su "100" per utilizzare una compressione più debole durante il rendering del documento.
// Ciò migliorerà la qualità dell'immagine al costo di una maggiore dimensione del file.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Mostra come convertire un intero documento in PDF con tre livelli nella struttura del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce le intestazioni dei livelli da 1 a 5.
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

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Il documento PDF di output conterrà uno schema, ovvero un sommario che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "4" per escludere tutte le intestazioni i cui livelli sono superiori a 4 dalla struttura.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Se una voce di profilo ha voci successive di un livello superiore tra se stessa e la voce successiva di livello uguale o inferiore,
// apparirà una freccia a sinistra della voce. Questa voce è il "proprietario" di molte di queste "sottovoci".
// Nel nostro documento, le voci dello schema del 5° livello di intestazione sono sottovoci della seconda voce dello schema del 4° livello,
 // le voci di 4° e 5° livello di intestazione sono sottovoci della seconda voce di 3° livello e così via.
// Nella struttura, possiamo fare clic sulla freccia della voce "proprietario" per comprimere/espandere tutte le sue sottovoci.
// Imposta la proprietà "ExpandedOutlineLevels" su "2" per espandere automaticamente tutte le voci del livello di intestazione 2 e della struttura inferiore
 // e comprime tutte le voci di livello e 3 e superiori quando apriamo il documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Guarda anche

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

---

## Save(Stream, SaveFormat) {#save}

Salva il documento in uno stream utilizzando il formato specificato.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Stream dove salvare il documento. |
| saveFormat | SaveFormat | Il formato in cui salvare il documento. |

### Valore di ritorno

Informazioni aggiuntive che puoi utilizzare facoltativamente.

### Esempi

Mostra come salvare un documento in uno stream.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Verifica che lo stream contenga il documento.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Mostra come salvare un documento in un'immagine tramite flusso e quindi leggere l'immagine da tale flusso.

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

                // Rilegge il flusso in un'immagine.
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

### Guarda anche

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

---

## Save(Stream, SaveOptions) {#save_1}

Salva il documento in uno stream utilizzando le opzioni di salvataggio specificate.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Stream dove salvare il documento. |
| saveOptions | SaveOptions | Specifica le opzioni che controllano la modalità di salvataggio del documento. Può essere null. Se questo è nullo, il documento verrà salvato nel formato binario DOC. |

### Valore di ritorno

Informazioni aggiuntive che puoi utilizzare facoltativamente.

### Esempi

Mostra come convertire solo alcune pagine di un documento in PDF.

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
    // Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui quel metodo converte il documento in .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Imposta "PageIndex" su "1" per eseguire il rendering di una parte del documento a partire dalla seconda pagina.
    options.PageSet = new PageSet(1);

    // Questo documento conterrà una pagina a partire dalla seconda pagina, che conterrà solo la seconda pagina.
    doc.Save(stream, options);
}
```

### Guarda anche

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

---

## Save(HttpResponse, string, ContentDisposition, SaveOptions) {#save_5}

Invia il documento al browser del client.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| response | HttpResponse | Oggetto risposta dove salvare il documento. |
| fileName | String | Il nome del documento che apparirà nel browser del client. Il nome non deve contenere il percorso. |
| contentDisposition | ContentDisposition | UN[`ContentDisposition`](../../contentdisposition/) value that specifica come il documento viene presentato al browser del client. |
| saveOptions | SaveOptions | Specifica le opzioni che controllano la modalità di salvataggio del documento. Può essere nullo. |

### Valore di ritorno

Informazioni aggiuntive che puoi utilizzare facoltativamente.

### Osservazioni

Internamente, questo metodo salva prima in un flusso di memoria e quindi copia nel flusso di risposta perché il flusso di risposta non supporta la ricerca.

### Esempi

Mostra come eseguire una stampa unione e quindi salvare il documento nel browser client.

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

// Invia il documento al browser del client.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Rilasciato perché HttpResponse è nullo nel test.

// Dovremo chiudere questa risposta manualmente per assicurarci di non aggiungere contenuto superfluo al documento dopo il salvataggio.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Guarda anche

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


