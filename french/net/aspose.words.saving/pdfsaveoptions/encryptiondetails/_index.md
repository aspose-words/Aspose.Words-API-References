---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words pour .NET
description: Découvrez la propriété EncryptionDetails de PdfSaveOptions pour configurer facilement les paramètres de cryptage PDF, garantissant ainsi que vos documents restent sécurisés et protégés.
type: docs
weight: 130
url: /fr/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Obtient ou définit les détails de cryptage du document PDF de sortie.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Remarques

La valeur par défaut est`nul` et le document de sortie ne sera pas chiffré. Lorsque cette propriété est définie sur une valeur valide[`PdfEncryptionDetails`](../../pdfencryptiondetails/)objet, alors le document PDF de sortie sera crypté.

L'algorithme de cryptage AES-128 est utilisé lors de l'enregistrement en conformité avec PDF 1.7 (y compris PDF/UA-1). L'algorithme de cryptage AES-256 est utilisé lors de l'enregistrement en conformité avec PDF 2.0.

Le chiffrement est interdit par la conformité PDF/A. Cette option sera ignorée lors de l'enregistrement au format PDF/A.

ContentCopyForAccessibility L'autorisation « conformité PDF/UA » est requise si le document de sortie est chiffré. Cette autorisation sera automatiquement utilisée lors de l'enregistrement au format PDF/UA.

ContentCopyForAccessibility l'autorisation est obsolète au format PDF 2.0. Cette autorisation sera ignorée lors de l'enregistrement au format PDF 2.0.

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
