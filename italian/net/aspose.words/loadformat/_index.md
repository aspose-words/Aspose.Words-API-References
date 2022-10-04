---
title: LoadFormat
second_title: Aspose.Words per .NET API Reference
description: Indica il formato del documento da caricare.
type: docs
weight: 3350
url: /it/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Indica il formato del documento da caricare.

```csharp
public enum LoadFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `0` | Indica ad Aspose.Words di riconoscere il formato automaticamente. |
| Doc | `10` | Documento Microsoft Word 95 o Word 97 - 2003. |
| Dot | `11` | Modello di Microsoft Word 95 o Word 97 - 2003. |
| DocPreWord60 | `12` | Il documento è nel formato precedente a Word 95. Aspose.Words attualmente non supporta il caricamento di tali documenti. |
| Docx | `20` | Documento Office Open XML WordprocessingML (senza macro). |
| Docm | `21` | Documento abilitato per le macro di Office Open XML WordprocessingML. |
| Dotx | `22` | Modello Office Open XML WordprocessingML (senza macro). |
| Dotm | `23` | Modello abilitato per le macro di Office Open XML WordprocessingML. |
| FlatOpc | `24` | Office Open XML WordprocessingML archiviato in un file XML piatto anziché in un pacchetto ZIP. |
| FlatOpcMacroEnabled | `25` | Documento con abilitazione macro per WordprocessingML Office Open XML archiviato in un file XML piatto anziché in un pacchetto ZIP. |
| FlatOpcTemplate | `26` | Modello Office Open XML WordprocessingML (senza macro) archiviato in un file XML piatto anziché in un pacchetto ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Modello abilitato per macro di WordprocessingML di Office Open XML archiviato in un file XML piatto anziché in un pacchetto ZIP. |
| Rtf | `30` | Formato RTF. |
| WordML | `31` | Formato WordprocessingML di Microsoft Word 2003. |
| Html | `50` | formato HTML. |
| Mhtml | `51` | Formato MHTML (archivio Web). |
| Mobi | `52` | formato MOBI. Utilizzato dal lettore MobiPocket e dai lettori Amazon Kindle. |
| Chm | `53` | Formato CHM (Guida HTML compilato). |
| Azw3 | `54` | formato AZW3. Utilizzato dai lettori Amazon Kindle. |
| Epub | `55` | formato EPUB. |
| Odt | `60` | Documento di testo ODF. |
| Ott | `61` | Modello di documento di testo ODF. |
| Text | `62` | Testo normale. |
| Markdown | `63` | Documento di testo Markdown. |
| Pdf | `64` | Documento PDF. |
| Xml | `65` | documento XML. |
| Unknown | `255` | Formato non riconosciuto, non può essere caricato da Aspose.Words. |

### Esempi

Mostra come salvare una pagina Web come file .docx.

```csharp
const string url = "http://www.aspose.com/";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // L'URL viene utilizzato di nuovo come baseUri per garantire che tutti i percorsi di immagine relativi vengano recuperati correttamente.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Carica il documento HTML dallo stream e passa l'oggetto LoadOptions.
        Document doc = new Document(stream, options);

        // A questo punto, possiamo leggere e modificare il contenuto del documento e quindi salvarlo nel file system locale.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Mostra come specificare un URI di base quando si apre un documento html.

```csharp
// Supponiamo di voler caricare un documento .html che contiene un'immagine collegata da un relativo URI
// mentre l'immagine si trova in una posizione diversa. In tal caso, dovremo risolvere l'URI relativo in uno assoluto.
 // Possiamo fornire un URI di base usando un oggetto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Mentre l'immagine era interrotta nell'input .html, il nostro URI di base personalizzato ci ha aiutato a riparare il collegamento.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Questo documento di output mostrerà l'immagine mancante.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

Mostra come utilizzare i metodi FileFormatUtil per rilevare il formato di un documento.

```csharp
// Carica un documento da un file a cui manca un'estensione, quindi rileva il formato del file.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Di seguito sono riportati due metodi per convertire un LoadFormat nel corrispondente SaveFormat.
    // 1 - Ottieni la stringa di estensione del file per LoadFormat, quindi ottieni il corrispondente SaveFormat da quella stringa:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Converti LoadFormat direttamente nel suo SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Carica un documento dallo stream, quindi salvalo con l'estensione file rilevata automaticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
