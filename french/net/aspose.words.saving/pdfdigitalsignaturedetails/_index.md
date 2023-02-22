---
title: Class PdfDigitalSignatureDetails
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.PdfDigitalSignatureDetails classe. Contient des détails pour signer un document PDF avec une signature numérique.
type: docs
weight: 5150
url: /fr/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

Contient des détails pour signer un document PDF avec une signature numérique.

```csharp
public class PdfDigitalSignatureDetails
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | Initialise une instance de cette classe. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(CertificateHolder, string, string, DateTime) | Initialise une instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Renvoie l'objet détenteur du certificat qui contient le certificat utilisé pour signer le document. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Obtient ou définit l'algorithme de hachage. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Obtient ou définit l'emplacement de la signature. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Obtient ou définit la raison de la signature. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Obtient ou définit la date de la signature. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Obtient ou définit les paramètres d'horodatage de la signature numérique. |

### Remarques

Pour le moment, la signature numérique de documents PDF n'est disponible que sur .NET 2.0 ou supérieur.

Pour signer numériquement un document PDF lorsqu'il est créé par Aspose.Words, définissez le[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) propriété à une propriété valide`PdfDigitalSignatureDetails` objet puis enregistrez le document au format PDF en passant le[`PdfSaveOptions`](../pdfsaveoptions/)comme paramètre dans le[`Save`](../../aspose.words/document/save/) méthode.

Aspose.Words crée une signature PKCS#7 sur l'ensemble du document PDF et utilise le filtre "Adobe.PPKMS" et le sous-filtre "adbe.pkcs7.sha1" lors de la création d'une signature numérique.

### Exemples

Montre comment signer un document PDF généré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configurez l'objet "DigitalSignatureDetails" de l'objet "SaveOptions" pour
// signe numériquement le document tel que nous le rendons avec la méthode "Save".
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


