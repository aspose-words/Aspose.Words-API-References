---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.LoadFormat, che definisce i formati dei documenti per un caricamento fluido e una maggiore compatibilità nelle tue applicazioni.
type: docs
weight: 4000
url: /it/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Indica il formato del documento che deve essere caricato.

```csharp
public enum LoadFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `0` | Indica ad Aspose.Words di riconoscere automaticamente il formato. |
| MsWorks | `8` | Documento di Microsoft Works 8. |
| Doc | `10` | Documento Microsoft Word 95 o Word 97 - 2003. |
| Dot | `11` | Modello di Microsoft Word 95 o Word 97 - 2003. |
| DocPreWord60 | `12` | Il documento è in un formato precedente a Word 95. Aspose.Words non supporta attualmente il caricamento di tali documenti. |
| Docx | `20` | Documento di elaborazione testi Office Open XML (senza macro). |
| Docm | `21` | Documento con macro abilitate per l'elaborazione di testi Office Open XML. |
| Dotx | `22` | Modello di elaborazione testi Office Open XML (senza macro). |
| Dotm | `23` | Modello con macro abilitate per Office Open XML WordprocessingML. |
| FlatOpc | `24` | Office Open XML WordprocessingML memorizzato in un file XML semplice anziché in un pacchetto ZIP. |
| FlatOpcMacroEnabled | `25` | Documento con macro abilitate per Office Open XML WordprocessingML memorizzato in un file XML semplice anziché in un pacchetto ZIP. |
| FlatOpcTemplate | `26` | Modello Office Open XML WordprocessingML (senza macro) memorizzato in un file XML semplice anziché in un pacchetto ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Modello con macro abilitate per Office Open XML WordprocessingML memorizzato in un file XML semplice anziché in un pacchetto ZIP. |
| Rtf | `30` | Formato RTF . |
| WordML | `31` | Formato ML per l'elaborazione testi di Microsoft Word 2003. |
| Html | `50` | Formato HTML. |
| Mhtml | `51` | Formato MHTML (archivio Web). |
| Mobi | `52` | Formato MOBI. Utilizzato dal lettore MobiPocket e dai lettori Kindle di Amazon. |
| Chm | `53` | Formato CHM (Guida HTML compilata). |
| Azw3 | `54` | Formato AZW3. Utilizzato dai lettori Kindle di Amazon. |
| Epub | `55` | Formato EPUB. |
| Odt | `60` | Documento di testo ODF. |
| Ott | `61` | Modello di documento di testo ODF. |
| Text | `62` | Testo normale. |
| Markdown | `63` | Documento di testo markdown. |
| Pdf | `64` | Documento PDF. |
| Xml | `65` | Documento XML. |
| Unknown | `255` | Formato non riconosciuto, non può essere caricato da Aspose.Words. |

## Esempi

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

Mostra come specificare un URI di base quando si apre un documento HTML.

```csharp
// Supponiamo di voler caricare un documento .html che contiene un'immagine collegata da un URI relativo
// mentre l'immagine si trova in una posizione diversa. In tal caso, dovremo risolvere l'URI relativo in uno assoluto.
 // Possiamo fornire un URI di base utilizzando un oggetto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Sebbene l'immagine fosse danneggiata nell'input .html, il nostro URI di base personalizzato ci ha aiutato a riparare il collegamento.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Questo documento di output visualizzerà l'immagine mancante.
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

    // Di seguito sono riportati due metodi per convertire un LoadFormat nel suo SaveFormat corrispondente.
    // 1 - Ottieni la stringa dell'estensione del file per LoadFormat, quindi ottieni il SaveFormat corrispondente da quella stringa:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Converti LoadFormat direttamente nel suo SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Carica un documento dal flusso e salvalo nell'estensione di file rilevata automaticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
