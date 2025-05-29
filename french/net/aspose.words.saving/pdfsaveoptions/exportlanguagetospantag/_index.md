---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ExportLanguageToSpanTag de PdfSaveOptions. Contrôlez l'exportation de la langue du texte avec les balises Span pour une structure et une accessibilité améliorées du document.
type: docs
weight: 150
url: /fr/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Obtient ou définit une valeur déterminant s'il faut ou non créer une balise « Span » dans la structure du document pour exporter la langue du texte.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`et l'attribut « Lang » est attaché à une séquence de contenu marqué dans un flux de contenu de page.

Lorsque la valeur est`vrai` La balise « Span » est créée pour le texte avec une langue non par défaut et l'attribut « Lang » est attaché à cette balise.

Cette valeur est ignorée lorsque[`ExportDocumentStructure`](../exportdocumentstructure/) est`FAUX` .

## Exemples

Montre comment créer une balise « Span » dans la structure du document pour exporter la langue du texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Remarque : lorsque « ExportDocumentStructure » est faux, « ExportLanguageToSpanTag » est ignoré.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
