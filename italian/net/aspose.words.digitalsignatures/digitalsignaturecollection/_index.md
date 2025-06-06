---
title: DigitalSignatureCollection Class
linktitle: DigitalSignatureCollection
articleTitle: DigitalSignatureCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words DigitalSignatureCollection, che offre un facile accesso a una raccolta di firme digitali di sola lettura per la gestione sicura dei documenti.
type: docs
weight: 590
url: /it/net/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class

Fornisce una raccolta di sola lettura di firme digitali allegate a un documento.

Per saperne di più, visita il[Lavorare con le firme digitali](https://docs.aspose.com/words/net/working-with-digital-signatures/) articolo di documentazione.

```csharp
public class DigitalSignatureCollection : IEnumerable<DigitalSignature>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [DigitalSignatureCollection](digitalsignaturecollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.digitalsignatures/digitalsignaturecollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/) { get; } | Restituisce`VERO`se tutte le firme digitali in questa raccolta sono valide e il documento non è stato manomesso with Restituisce anche`VERO` se non ci sono firme digitali. Restituisce`falso` se almeno una firma digitale non è valida. |
| [Item](../../aspose.words.digitalsignatures/digitalsignaturecollection/item/) { get; } | Ottiene una firma del documento all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/)() | Restituisce un oggetto enumeratore del dizionario che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |

## Osservazioni

[`DigitalSignatures`](../../aspose.words/document/digitalsignatures/)

## Esempi

Mostra come convalidare e visualizzare le informazioni su ciascuna firma in un documento.

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

* class [DigitalSignature](../digitalsignature/)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../)
