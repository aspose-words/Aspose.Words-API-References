---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.FileFormatInfo per un rilevamento efficiente del formato dei documenti. Accedi a dati dettagliati per migliorare le tue soluzioni di gestione dei file.
type: docs
weight: 3220
url: /it/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Contiene i dati restituiti da[`FileFormatUtil`](../fileformatutil/) metodi di rilevamento del formato del documento.

Per saperne di più, visita il[Rileva il formato del file e controlla la compatibilità del formato](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) articolo di documentazione.

```csharp
public class FileFormatInfo
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Ottiene la codifica rilevata se applicabile al formato del documento corrente. Al momento rileva la codifica solo per i documenti HTML. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Restituisce`VERO`se questo documento contiene una firma digitale. Questa proprietà informa semplicemente che una firma digitale è presente su un documento, ma non specifica se la firma è valida o meno. |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | Restituisce`VERO` se questo documento contiene macro VBA. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Restituisce`VERO` se il documento è crittografato e richiede una password per aprirlo. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Ottiene il formato del documento rilevato. |

## Osservazioni

Non è possibile creare istanze di questa classe direttamente. Gli oggetti di questa classe vengono restituiti da [`DetectFileFormat`](../fileformatutil/detectfileformat/) metodi.

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
