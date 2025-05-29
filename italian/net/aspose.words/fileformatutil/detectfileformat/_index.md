---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: Aspose.Words per .NET
description: Identifica rapidamente i formati dei documenti con il metodo DetectFileFormat di FileFormatUtil. Ottieni informazioni accurate sui formati per una gestione efficiente dei file.
type: docs
weight: 30
url: /it/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

Rileva e restituisce le informazioni sul formato di un documento memorizzato in un file su disco.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome del file. |

### Valore di ritorno

UN[`FileFormatInfo`](../../fileformatinfo/) oggetto che contiene le informazioni rilevate.

## Osservazioni

Anche se questo metodo rileva il formato del documento, non garantisce che il documento specificato sia valido. Questo metodo rileva il formato del documento solo leggendo dati sufficienti per il rilevamento. Per verificare completamente la validità di un documento, è necessario caricarlo in un[`Document`](../../document/) oggetto.

Questo metodo genera[`FileCorruptedException`](../../filecorruptedexception/) quando il formato è riconosciuto, ma il rilevamento non può essere completato a causa di danneggiamento.

## Esempi

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato e la crittografia del documento.

```csharp
Document doc = new Document();

// Configura un oggetto SaveOptions per crittografare il documento
// con una password quando lo salviamo, e poi salviamo il documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verificare il tipo di file del nostro documento e il suo stato di crittografia.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la presenza di firme digitali.

```csharp
// Utilizzare un'istanza di FileFormatInfo per verificare che un documento non sia firmato digitalmente.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Utilizzare un nuovo FileFormatInstance per confermare che è firmato.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Possiamo caricare e accedere alle firme di un documento firmato in una raccolta come questa.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Guarda anche

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## DetectFileFormat(*Stream*) {#detectfileformat}

Rileva e restituisce le informazioni sul formato di un documento memorizzato in un flusso.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso. |

### Valore di ritorno

UN[`FileFormatInfo`](../../fileformatinfo/) oggetto che contiene le informazioni rilevate.

## Osservazioni

Il flusso deve essere posizionato all'inizio del documento.

Quando questo metodo ritorna, la posizione nel flusso viene ripristinata alla posizione originale.

Anche se questo metodo rileva il formato del documento, non garantisce che il documento specificato sia valido. Questo metodo rileva il formato del documento solo leggendo dati sufficienti per il rilevamento. Per verificare completamente la validità di un documento, è necessario caricarlo in un[`Document`](../../document/) oggetto.

Questo metodo genera[`FileCorruptedException`](../../filecorruptedexception/) quando il formato è riconosciuto, ma il rilevamento non può essere completato a causa di danneggiamento.

## Esempi

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

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
