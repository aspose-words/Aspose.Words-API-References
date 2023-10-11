---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Obtient ou définit une valeur déterminant si un graphique de paragraphe doit être marqué comme artefact.
type: docs
weight: 160
url: /fr/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Obtient ou définit une valeur déterminant si un graphique de paragraphe doit être marqué comme artefact.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

### Remarques

La valeur par défaut est`FAUX` et les graphiques de paragraphe (soulignés, accentuation du texte, etc.) seront marqués comme « Span » dans la structure logique du document.

Lorsque la valeur est`vrai` les graphiques du paragraphe seront marqués comme « Artefact ».

Cette valeur est ignorée lorsque[`ExportDocumentStructure`](../exportdocumentstructure/) est`FAUX` .

### Exemples

Montre comment exporter des graphiques de paragraphe sous forme d'artefacts (soulignés, accentuation du texte, etc.).

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


