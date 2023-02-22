---
title: Enum PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.PdfDigitalSignatureHashAlgorithm enum. Specifica un algoritmo hash digitale utilizzato da una firma digitale.
type: docs
weight: 5160
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

### Esempi

Mostra come firmare un documento PDF generato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configura l'oggetto "DigitalSignatureDetails" dell'oggetto "SaveOptions" su
// Firma digitalmente il documento mentre lo eseguiamo con il metodo "Salva".
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


