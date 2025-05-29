---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.PdfDigitalSignatureDetails per una firma digitale PDF senza interruzioni. Migliora la sicurezza dei documenti con una facile integrazione e funzionalità affidabili.
type: docs
weight: 6220
url: /it/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

Contiene i dettagli per firmare un documento PDF con una firma digitale.

```csharp
public class PdfDigitalSignatureDetails
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | Inizializza un'istanza di questa classe. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) | Inizializza un'istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Restituisce l'oggetto titolare del certificato che contiene il certificato utilizzato per firmare il documento. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Ottiene o imposta l'algoritmo hash. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Ottiene o imposta la posizione della firma. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Ottiene o imposta il motivo della firma. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Ottiene o imposta la data della firma. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Ottiene o imposta le impostazioni di timestamp della firma digitale. |

## Osservazioni

Al momento la firma digitale dei documenti PDF è disponibile solo su .NET 3.5 o versioni successive.

Per firmare digitalmente un documento PDF quando viene creato da Aspose.Words, impostare[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) proprietà a un valido`PdfDigitalSignatureDetails` oggetto e quindi salvare il documento nel formato PDF passando il[`PdfSaveOptions`](../pdfsaveoptions/) come parametro nel[`Save`](../../aspose.words/document/save/) metodo.

Aspose.Words crea una firma PKCS#7 sull'intero documento PDF e utilizza il filtro "Adobe.PPKMS" e il sottofiltro "adbe.pkcs7.sha1" durante la creazione di una firma digitale.

## Esempi

Mostra come firmare un documento PDF generato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configurare l'oggetto "DigitalSignatureDetails" dell'oggetto "SaveOptions" su
// firmare digitalmente il documento mentre lo riproduciamo con il metodo "Salva".
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());
Assert.AreEqual(certificateHolder, options.DigitalSignatureDetails.CertificateHolder);

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
