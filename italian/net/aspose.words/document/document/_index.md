---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words per .NET
description: Crea facilmente documenti Word vuoti con il nostro intuitivo strumento di creazione documenti. Semplifica il tuo processo di scrittura oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words/document/document/
---
## Document() {#constructor}

Crea un documento Word vuoto.

```csharp
public Document()
```

## Osservazioni

Un documento vuoto viene recuperato dalle risorse e, per impostazione predefinita, il documento risultante sembra più simile a quello creato daWord2007. Questo documento vuoto contiene una tabella di caratteri predefiniti, stili predefiniti minimi e stili latenti.

[`OptimizeFor`](../../../aspose.words.settings/compatibilityoptions/optimizefor/) Il metodo può essere utilizzato per ottimizzare il contenuto del documento e il comportamento predefinito di Aspose.Words per una particolare versione di MS Word.

Il formato carta predefinito del documento è Lettera. Se si desidera modificare l'impostazione di pagina, utilizzare [`PageSetup`](../../section/pagesetup/).

Dopo la creazione, puoi utilizzare[`DocumentBuilder`](../../documentbuilder/) per aggiungere facilmente contenuti al documento.

## Esempi

Mostra come formattare una sequenza di testo utilizzando la proprietà font.

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

Mostra come creare un documento semplice.

```csharp
Document doc = new Document();

// I nuovi oggetti Documento vengono forniti per impostazione predefinita con il set minimo di nodi
// necessario per iniziare ad aggiungere contenuti quali testo e forme: una sezione, un corpo e un paragrafo.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

Mostra come creare e caricare documenti.

```csharp
// Esistono due modi per creare un oggetto Document utilizzando Aspose.Words.
// 1 - Crea un documento vuoto:
Document doc = new Document();

// I nuovi oggetti Documento vengono forniti per impostazione predefinita con il set minimo di nodi
// necessario per iniziare ad aggiungere contenuti quali testo e forme: una sezione, un corpo e un paragrafo.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Carica un documento presente nel file system locale:
doc = new Document(MyDir + "Document.docx");

// I documenti caricati avranno contenuti a cui potremo accedere e che potremo modificare.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Alcune operazioni che devono essere eseguite durante il caricamento, come l'utilizzo di una password per decrittografare un documento,
// può essere fatto passando un oggetto LoadOptions durante il caricamento del documento.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

Apre un documento esistente da un file. Rileva automaticamente il formato del file.

```csharp
public Document(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome del file del documento da aprire. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Il formato del documento non è riconosciuto o non è supportato. |
| [FileCorruptedException](../../filecorruptedexception/) | Il documento sembra danneggiato e non può essere caricato. |
| Exception | C'è un problema con il documento e dovrebbe essere segnalato agli sviluppatori di Aspose.Words. |
| IOException | C'è un'eccezione di input/output. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Il documento è crittografato e richiede una password per essere aperto, ma hai fornito una password errata. |
| ArgumentException | Il nome del file non può essere nullo o una stringa vuota. |

## Esempi

Mostra come aprire un documento e convertirlo in formato PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Mostra come convertire un PDF in un file .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Carichiamo il documento PDF appena salvato e convertiamolo in .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Mostra come caricare un PDF.

```csharp
Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// Di seguito sono riportati due metodi per caricare documenti PDF utilizzando i prodotti Aspose.
// 1 - Carica come documento Aspose.Words:
Document asposeWordsDoc = new Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Carica come documento Aspose.Pdf:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

Apre un documento esistente da un file. Permette di specificare opzioni aggiuntive come una password di crittografia.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome del file del documento da aprire. |
| loadOptions | LoadOptions | Opzioni aggiuntive da utilizzare durante il caricamento di un documento. Possono essere`null`. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Il formato del documento non è riconosciuto o non è supportato. |
| [FileCorruptedException](../../filecorruptedexception/) | Il documento sembra danneggiato e non può essere caricato. |
| Exception | C'è un problema con il documento e dovrebbe essere segnalato agli sviluppatori di Aspose.Words. |
| IOException | C'è un'eccezione di input/output. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Il documento è crittografato e richiede una password per essere aperto, ma hai fornito una password errata. |
| ArgumentException | Il nome del file non può essere nullo o una stringa vuota. |

## Esempi

Mostra come caricare un documento Microsoft Word crittografato.

```csharp
Document doc;

// Aspose.Words genera un'eccezione se proviamo ad aprire un documento crittografato senza la relativa password.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Quando si carica un documento di questo tipo, la password viene passata al costruttore del documento tramite un oggetto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Esistono due modi per caricare un documento crittografato con un oggetto LoadOptions.
// 1 - Carica il documento dal file system locale in base al nome file:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Carica il documento da un flusso:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Mostra come creare e caricare documenti.

```csharp
// Esistono due modi per creare un oggetto Document utilizzando Aspose.Words.
// 1 - Crea un documento vuoto:
Document doc = new Document();

// I nuovi oggetti Documento vengono forniti per impostazione predefinita con il set minimo di nodi
// necessario per iniziare ad aggiungere contenuti quali testo e forme: una sezione, un corpo e un paragrafo.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Carica un documento presente nel file system locale:
doc = new Document(MyDir + "Document.docx");

// I documenti caricati avranno contenuti a cui potremo accedere e che potremo modificare.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Alcune operazioni che devono essere eseguite durante il caricamento, come l'utilizzo di una password per decrittografare un documento,
// può essere fatto passando un oggetto LoadOptions durante il caricamento del documento.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

Apre un documento esistente da un flusso. Rileva automaticamente il formato del file.

```csharp
public Document(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Flusso da cui caricare il documento. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Il formato del documento non è riconosciuto o non è supportato. |
| [FileCorruptedException](../../filecorruptedexception/) | Il documento sembra danneggiato e non può essere caricato. |
| Exception | C'è un problema con il documento e dovrebbe essere segnalato agli sviluppatori di Aspose.Words. |
| IOException | C'è un'eccezione di input/output. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Il documento è crittografato e richiede una password per essere aperto, ma hai fornito una password errata. |
| ArgumentNullException | Il flusso non può essere nullo. |
| NotSupportedException | Il flusso non supporta la lettura o la ricerca. |
| ObjectDisposedException | Il flusso è un oggetto disposto. |

## Osservazioni

Il documento deve essere memorizzato all'inizio del flusso. Il flusso deve supportare il posizionamento casuale.

## Esempi

Mostra come caricare un documento utilizzando un flusso.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Mostra come caricare un documento da un URL.

```csharp
// Crea un URL che punti a un documento Microsoft Word.
const string url = "https://filesamples.com/samples/document/docx/sample3.docx";

// Scarica il documento in un array di byte, quindi carica quell'array in un documento utilizzando un flusso di memoria.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // A questo punto possiamo leggere e modificare il contenuto del documento e poi salvarlo nel file system locale.
        Assert.AreEqual("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
                        "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
                        "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.",
            doc.FirstSection.Body.Paragraphs[3].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

Apre un documento esistente da un flusso. Permette di specificare opzioni aggiuntive come una password di crittografia.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso da cui caricare il documento. |
| loadOptions | LoadOptions | Opzioni aggiuntive da utilizzare durante il caricamento di un documento. Possono essere`null`. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Il formato del documento non è riconosciuto o non è supportato. |
| [FileCorruptedException](../../filecorruptedexception/) | Il documento sembra danneggiato e non può essere caricato. |
| Exception | C'è un problema con il documento e dovrebbe essere segnalato agli sviluppatori di Aspose.Words. |
| IOException | C'è un'eccezione di input/output. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Il documento è crittografato e richiede una password per essere aperto, ma hai fornito una password errata. |
| ArgumentNullException | Il flusso non può essere nullo. |
| NotSupportedException | Il flusso non supporta la lettura o la ricerca. |
| ObjectDisposedException | Il flusso è un oggetto disposto. |

## Osservazioni

Il documento deve essere memorizzato all'inizio del flusso. Il flusso deve supportare il posizionamento casuale.

## Esempi

Mostra come aprire un documento HTML con immagini da un flusso utilizzando un URI di base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Passare l'URI della cartella base durante il caricamento
    // in modo che sia possibile trovare tutte le immagini con URI relativi nel documento HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifica che la prima forma del documento contenga un'immagine valida.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

Mostra come salvare una pagina web come file .docx.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // L'URL viene utilizzato nuovamente come baseUri per garantire che tutti i percorsi immagine relativi vengano recuperati correttamente.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Carica il documento HTML dal flusso e passa l'oggetto LoadOptions.
        Document doc = new Document(stream, options);

        // A questo punto possiamo leggere e modificare il contenuto del documento e poi salvarlo nel file system locale.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Mostra come caricare un documento Microsoft Word crittografato.

```csharp
Document doc;

// Aspose.Words genera un'eccezione se proviamo ad aprire un documento crittografato senza la relativa password.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Quando si carica un documento di questo tipo, la password viene passata al costruttore del documento tramite un oggetto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Esistono due modi per caricare un documento crittografato con un oggetto LoadOptions.
// 1 - Carica il documento dal file system locale in base al nome file:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Carica il documento da un flusso:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
