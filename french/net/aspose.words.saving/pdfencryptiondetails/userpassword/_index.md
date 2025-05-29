---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété UserPassword améliore la sécurité des PDF en exigeant un mot de passe pour l'accès, garantissant ainsi que vos documents restent protégés et confidentiels.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Spécifie le mot de passe utilisateur requis pour ouvrir le document PDF crypté.

```csharp
public string UserPassword { get; set; }
```

## Remarques

Le mot de passe utilisateur sera requis pour ouvrir un document PDF chiffré et le consulter. Les autorisations spécifiées dans [`Permissions`](../permissions/) sera appliqué par le logiciel de lecture.

Le mot de passe de l'utilisateur peut être`nul` ou chaîne vide ; dans ce cas, aucun mot de passe ne sera demandé à l'utilisateur lors de l'ouverture du document PDF. Le mot de passe de l'utilisateur ne peut pas être identique à celui du propriétaire.

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

* class [PdfEncryptionDetails](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
