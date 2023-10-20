---
title: DigitalSignature.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words per .NET
description: DigitalSignature CertificateHolder proprietà. Restituisce loggetto titolare del certificato che contiene il certificato utilizzato per firmare il documento in C#.
type: docs
weight: 10
url: /it/net/aspose.words.digitalsignatures/digitalsignature/certificateholder/
---
## DigitalSignature.CertificateHolder property

Restituisce l'oggetto titolare del certificato che contiene il certificato utilizzato per firmare il documento.

```csharp
public CertificateHolder CertificateHolder { get; }
```

## Esempi

Mostra come firmare documenti con certificati X.509.

```csharp
// Verifica che un documento non sia firmato.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crea un oggetto CertificateHolder da un file PKCS12, che utilizzeremo per firmare il documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Esistono due modi per salvare una copia firmata di un documento nel file system locale:
// 1 - Designa un documento con un nome file di sistema locale e salva una copia firmata in una posizione specificata da un altro nome file.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Prendi un documento da uno stream e salva una copia firmata in un altro stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Verifica che tutte le firme digitali del documento siano valide e controllane i dettagli.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Guarda anche

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignature](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
