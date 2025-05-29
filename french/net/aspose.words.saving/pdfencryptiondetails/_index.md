---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.PdfEncryptionDetails pour un cryptage PDF sécurisé et des autorisations d'accès personnalisables, garantissant que vos documents restent protégés.
type: docs
weight: 6250
url: /fr/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Contient des détails sur le cryptage et les autorisations d'accès pour un document PDF.

Pour en savoir plus, visitez le[Protéger ou crypter un document](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) article de documentation.

```csharp
public class PdfEncryptionDetails
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(*string, string*) | Initialise une instance de cette classe. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(*string, string, [PdfPermissions](../pdfpermissions/)*) | Initialise une instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Spécifie le mot de passe du propriétaire du document PDF chiffré. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Spécifie les opérations autorisées à un utilisateur sur un document PDF chiffré. La valeur par défaut estDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Spécifie le mot de passe utilisateur requis pour ouvrir le document PDF crypté. |

## Exemples

Montre comment définir des autorisations sur un document PDF enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Étendez les autorisations pour permettre la modification des annotations.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Activer le cryptage via la propriété « EncryptionDetails ».
saveOptions.EncryptionDetails = encryptionDetails;

// Lorsque nous ouvrons ce document, nous devrons fournir le mot de passe avant d'accéder à son contenu.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
