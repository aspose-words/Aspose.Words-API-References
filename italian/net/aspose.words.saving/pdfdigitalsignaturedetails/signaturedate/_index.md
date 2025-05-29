---
title: PdfDigitalSignatureDetails.SignatureDate
linktitle: SignatureDate
articleTitle: SignatureDate
second_title: Aspose.Words per .NET
description: Scopri la proprietà SignatureDate di PdfDigitalSignatureDetails per gestire e personalizzare facilmente le date di firma dei tuoi documenti. Migliora il tuo flusso di lavoro digitale oggi stesso!
type: docs
weight: 60
url: /it/net/aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/
---
## PdfDigitalSignatureDetails.SignatureDate property

Ottiene o imposta la data della firma.

```csharp
public DateTime SignatureDate { get; set; }
```

## Osservazioni

Il valore predefinito è l'ora corrente.

Questo valore apparirà nella firma digitale come orario del computer non verificato.

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

* class [PdfDigitalSignatureDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
