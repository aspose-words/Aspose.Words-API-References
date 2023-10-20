---
title: PdfSaveOptions.EmbedAttachments
linktitle: EmbedAttachments
articleTitle: EmbedAttachments
second_title: Aspose.Words pour .NET
description: PdfSaveOptions EmbedAttachments propriété. Obtient ou définit une valeur déterminant sil faut ou non intégrer les pièces jointes au document PDF en C#.
type: docs
weight: 110
url: /fr/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

Obtient ou définit une valeur déterminant s'il faut ou non intégrer les pièces jointes au document PDF.

```csharp
public bool EmbedAttachments { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`et les pièces jointes ne sont pas intégrées.

Lorsque la valeur est`vrai` les pièces jointes sont intégrées au document PDF.

L'intégration de pièces jointes n'est pas prise en charge lors de l'enregistrement au format PDF/A et en conformité avec PDF/UA. `FAUX` la valeur sera utilisée automatiquement.

L'intégration de pièces jointes n'est pas prise en charge lorsque le cryptage est activé.`FAUX` value sera utilisé automatiquement.

## Exemples

Montre comment ajouter des pièces jointes intégrées au document PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
