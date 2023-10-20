---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words pour .NET
description: PdfEncryptionDetails UserPassword propriété. Spécifie le mot de passe utilisateur requis pour ouvrir le document PDF crypté en C#.
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

Le mot de passe utilisateur sera requis pour ouvrir un document PDF crypté et le visualiser. Les autorisations spécifiées dans [`Permissions`](../permissions/) sera appliqué par le logiciel de lecture.

Le mot de passe de l'utilisateur peut être`nul` ou une chaîne vide, dans ce cas aucun mot de passe ne sera demandé à l'utilisateur lors de l'ouverture du document PDF. Le mot de passe utilisateur ne peut pas être le même que le mot de passe propriétaire.

## Exemples

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

* class [PdfEncryptionDetails](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
