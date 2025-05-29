---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.PdfDigitalSignatureDetails pour une signature numérique PDF fluide. Améliorez la sécurité de vos documents grâce à une intégration facile et des fonctionnalités robustes.
type: docs
weight: 6220
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
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) | Initialise une instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Renvoie l'objet titulaire du certificat qui contient le certificat utilisé pour signer le document. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Obtient ou définit l'algorithme de hachage. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Obtient ou définit l'emplacement de la signature. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Obtient ou définit la raison de la signature. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Obtient ou définit la date de la signature. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Obtient ou définit les paramètres d'horodatage de la signature numérique. |

## Remarques

Pour le moment, la signature numérique des documents PDF n'est disponible que sur .NET 3.5 ou supérieur.

Pour signer numériquement un document PDF lorsqu'il est créé par Aspose.Words, définissez le[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) propriété à une valeur valide`PdfDigitalSignatureDetails` objet puis enregistrez le document au format PDF en passant le[`PdfSaveOptions`](../pdfsaveoptions/) comme paramètre dans le[`Save`](../../aspose.words/document/save/) méthode.

Aspose.Words crée une signature PKCS#7 sur l'ensemble du document PDF et utilise le filtre "Adobe.PPKMS" et le sous-filtre "adbe.pkcs7.sha1" lors de la création d'une signature numérique.

## Exemples

Montre comment signer un document PDF généré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configurez l'objet « DigitalSignatureDetails » de l'objet « SaveOptions » pour
// signer numériquement le document tel que nous le rendons avec la méthode « Enregistrer ».
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

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
