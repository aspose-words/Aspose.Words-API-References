---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words pour .NET
description: PdfEncryptionDetails constructeur. Initialise une instance de cette classe en C#.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails(*string, string*) {#constructor}

Initialise une instance de cette classe.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword)
```

### Voir également

* class [PdfEncryptionDetails](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

---

## PdfEncryptionDetails(*string, string, [PdfPermissions](../../pdfpermissions/)*) {#constructor_1}

Initialise une instance de cette classe.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword, PdfPermissions permissions)
```

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
