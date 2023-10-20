---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words pour .NET
description: PdfSaveOptions EncryptionDetails propriété. Obtient ou définit les détails de cryptage du document PDF de sortie en C#.
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

La valeur par défaut est`nul` et le document de sortie ne sera pas chiffré. Lorsque cette propriété est définie sur une valeur valide[`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, alors le document PDF de sortie sera crypté.

L'algorithme de cryptage AES-128 est utilisé lors de l'enregistrement au format PDF 1.7 (y compris PDF/UA-1). L'algorithme de cryptage AES-256 est utilisé lors de l'enregistrement au format PDF 2.0.

Le cryptage est interdit par la conformité PDF/A. Cette option sera ignorée lors de l'enregistrement au format PDF/A.

ContentCopyForAccessibility l'autorisation est requise par PDF/UA Compliance si le document de sortie est crypté. Cette autorisation sera automatiquement utilisée lors de l'enregistrement au format PDF/UA.

ContentCopyForAccessibility l'autorisation est obsolète au format PDF 2.0. Cette autorisation sera ignorée lors de l'enregistrement au format PDF 2.0.

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
