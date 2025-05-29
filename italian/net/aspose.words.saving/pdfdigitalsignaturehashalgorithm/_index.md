---
title: PdfDigitalSignatureHashAlgorithm Enum
linktitle: PdfDigitalSignatureHashAlgorithm
articleTitle: PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words PdfDigitalSignatureHashAlgorithm, che definisce algoritmi hash digitali per firme digitali sicure nei tuoi documenti.
type: docs
weight: 6230
url: /it/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

Specifica un algoritmo hash digitale utilizzato da una firma digitale.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Sha256 | `0` | Algoritmo hash SHA-256. |
| Sha384 | `1` | Algoritmo hash SHA-384. |
| Sha512 | `2` | Algoritmo hash SHA-512. |
| RipeMD160 | `3` | Algoritmo hash RIPEMD-160. |

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
