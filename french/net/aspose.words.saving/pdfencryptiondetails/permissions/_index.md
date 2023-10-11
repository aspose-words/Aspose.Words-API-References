---
title: PdfEncryptionDetails.Permissions
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfEncryptionDetails propriété. Spécifie les opérations autorisées à un utilisateur sur un document PDF crypté. La valeur par défaut estDisallowAll .
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Spécifie les opérations autorisées à un utilisateur sur un document PDF crypté. La valeur par défaut estDisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* espace de noms [Aspose.Words.Saving](../../pdfencryptiondetails/)
* Assemblée [Aspose.Words](../../../)


