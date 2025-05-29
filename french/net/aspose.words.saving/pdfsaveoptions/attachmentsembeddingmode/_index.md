---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: Aspose.Words pour .NET
description: Personnalisez l'intégration des pièces jointes aux PDF avec PdfSaveOptions. Assurez une intégration fluide et un partage optimisé des documents.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

Obtient ou définit une valeur déterminant la manière dont les pièces jointes sont intégrées au document PDF.

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## Remarques

La valeur par défaut estNone et les pièces jointes ne sont pas intégrées.

Les normes PDF/A-1, PDF/A-2 et PDF/A-4 standard (pas PDF/A-4f) n'autorisent pas les fichiers intégrés. None la valeur sera utilisée automatiquement.

## Exemples

Montre comment ajouter des pièces jointes intégrées au document PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### Voir également

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
