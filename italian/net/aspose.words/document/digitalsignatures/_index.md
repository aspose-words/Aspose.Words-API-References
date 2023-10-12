---
title: Document.DigitalSignatures
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Ottiene la raccolta di firme digitali per questo documento e i relativi risultati di convalida.
type: docs
weight: 100
url: /it/net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

Ottiene la raccolta di firme digitali per questo documento e i relativi risultati di convalida.

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

### Osservazioni

Questa raccolta contiene firme digitali caricate dal documento originale. Queste firme digitali non verranno salvate quando salvi questo[`Document`](../) object in un file o flusso perché il salvataggio o la conversione produrrà un documento diverso dall'originale e le firme digitali originali non saranno più valide.

Questa collezione non lo è mai`nullo`. Se il documento non è firmato, conterrà zero elementi.

### Esempi

Mostra come convalidare e visualizzare informazioni su ciascuna firma in un documento.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}"); 
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

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

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


