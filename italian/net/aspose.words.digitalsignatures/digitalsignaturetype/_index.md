---
title: DigitalSignatureType Enum
linktitle: DigitalSignatureType
articleTitle: DigitalSignatureType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.DigitalSignatures.DigitalSignatureType per migliorare la sicurezza dei tuoi documenti con opzioni versatili di firma digitale.
type: docs
weight: 600
url: /it/net/aspose.words.digitalsignatures/digitalsignaturetype/
---
## DigitalSignatureType enumeration

Specifica il tipo di firma digitale.

```csharp
public enum DigitalSignatureType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Unknown | `0` | Indica un errore, tipo di firma digitale sconosciuto. |
| CryptoApi | `1` | Metodo di firma Crypto API utilizzato nei documenti binari .DOC di Microsoft Word 97-2003. |
| XmlDsig | `2` | Metodo di firma XmlDsig utilizzato nei documenti OOXML e OpenDocument. |

## Esempi

Mostra come firmare documenti con certificati X.509.

```csharp
// Verifica che un documento non sia firmato.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crea un oggetto CertificateHolder da un file PKCS12, che utilizzeremo per firmare il documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Esistono due modi per salvare una copia firmata di un documento nel file system locale:
// 1 - Designa un documento tramite un nome file di sistema locale e salva una copia firmata in una posizione specificata da un altro nome file.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Prendi un documento da un flusso e salva una copia firmata in un altro flusso.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Si prega di verificare che tutte le firme digitali del documento siano valide e di controllarne i dettagli.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../)
