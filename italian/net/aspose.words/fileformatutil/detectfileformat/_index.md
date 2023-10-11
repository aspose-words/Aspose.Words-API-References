---
title: FileFormatUtil.DetectFileFormat
second_title: Aspose.Words per .NET API Reference
description: FileFormatUtil metodo. Rileva e restituisce le informazioni su un formato di un documento archiviato in un file su disco.
type: docs
weight: 30
url: /it/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(string) {#detectfileformat_1}

Rileva e restituisce le informazioni su un formato di un documento archiviato in un file su disco.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome del file. |

### Valore di ritorno

UN[`FileFormatInfo`](../../fileformatinfo/) oggetto che contiene le informazioni rilevate.

### Osservazioni

Anche se questo metodo rileva il formato del documento, non garantisce che il documento specificato sia valido. Questo metodo rileva solo il formato del documento leggendo i dati sufficienti per il rilevamento. Per verificare completamente che un documento sia valido è necessario caricare il documento in a[`Document`](../../document/) oggetto.

Questo metodo lancia[`FileCorruptedException`](../../filecorruptedexception/) quando il formato viene riconosciuto , ma il rilevamento non può essere completato a causa di corruzione.

### Esempi

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato e la crittografia del documento.

```csharp
Document doc = new Document();

// Configura un oggetto SaveOptions per crittografare il documento
// con una password quando lo salviamo, quindi salviamo il documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verifica il tipo di file del nostro documento e il suo stato di crittografia.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la presenza di firme digitali.

```csharp
// Utilizzare un'istanza FileFormatInfo per verificare che un documento non sia firmato digitalmente.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// Utilizza una nuova FileFormatInstance per confermare che sia firmata.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Possiamo caricare e accedere alle firme di un documento firmato in una raccolta come questa.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Guarda anche

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../fileformatutil/)
* assemblea [Aspose.Words](../../../)

---

## DetectFileFormat(Stream) {#detectfileformat}

Rileva e restituisce le informazioni su un formato di un documento archiviato in uno stream.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso. |

### Valore di ritorno

UN[`FileFormatInfo`](../../fileformatinfo/) oggetto che contiene le informazioni rilevate.

### Osservazioni

Lo stream deve essere posizionato all'inizio del documento.

Quando questo metodo termina, la posizione nel flusso viene ripristinata nella posizione originale.

Anche se questo metodo rileva il formato del documento, non garantisce che il documento specificato sia valido. Questo metodo rileva solo il formato del documento leggendo i dati sufficienti per il rilevamento. Per verificare completamente che un documento sia valido è necessario caricare il documento in a[`Document`](../../document/) oggetto.

Questo metodo lancia[`FileCorruptedException`](../../filecorruptedexception/) quando il formato viene riconosciuto , ma il rilevamento non può essere completato a causa di corruzione.

### Esempi

Mostra come utilizzare i metodi FileFormatUtil per rilevare il formato di un documento.

```csharp
// Carica un documento da un file a cui manca un'estensione di file, quindi rileva il formato del file.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Di seguito sono riportati due metodi per convertire un LoadFormat nel corrispondente SaveFormat.
    // 1 - Ottieni la stringa dell'estensione del file per LoadFormat, quindi ottieni il corrispondente SaveFormat da quella stringa:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Converti LoadFormat direttamente nel suo SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Carica un documento dallo stream, quindi salvalo nell'estensione di file rilevata automaticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Guarda anche

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../fileformatutil/)
* assemblea [Aspose.Words](../../../)


