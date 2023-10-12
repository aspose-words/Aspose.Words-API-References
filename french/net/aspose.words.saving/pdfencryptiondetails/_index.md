---
title: Class PdfEncryptionDetails
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.PdfEncryptionDetails classe. Contient des détails sur le cryptage et les autorisations daccès à un document PDF.
type: docs
weight: 5460
url: /fr/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Contient des détails sur le cryptage et les autorisations d'accès à un document PDF.

Pour en savoir plus, visitez le[Protéger ou chiffrer un document](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) article documentaire.

```csharp
public class PdfEncryptionDetails
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(string, string) | Initialise une instance de cette classe. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(string, string, PdfPermissions) | Initialise une instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Spécifie le mot de passe du propriétaire du document PDF crypté. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Spécifie les opérations autorisées à un utilisateur sur un document PDF crypté. La valeur par défaut estDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Spécifie le mot de passe utilisateur requis pour ouvrir le document PDF crypté. |

### Exemples

Montre comment définir les autorisations sur un document PDF enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Étendre les autorisations pour permettre la modification des annotations.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Activer le chiffrement via la propriété "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// Lorsque nous ouvrirons ce document, nous devrons fournir le mot de passe avant d'accéder à son contenu.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


