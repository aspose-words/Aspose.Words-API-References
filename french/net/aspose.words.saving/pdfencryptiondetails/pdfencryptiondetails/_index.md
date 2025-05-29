---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur PdfEncryptionDetails pour initialiser facilement des instances de chiffrement PDF sécurisées. Améliorez la protection de vos documents grâce à notre puissant outil !
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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
