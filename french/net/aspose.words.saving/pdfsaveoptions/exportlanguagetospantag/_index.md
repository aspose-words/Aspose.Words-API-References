---
title: ExportLanguageToSpanTag
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit une valeur déterminant sil faut ou non créer une balise Span dans la structure du document pour exporter la langue du texte.
type: docs
weight: 130
url: /fr/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Obtient ou définit une valeur déterminant s'il faut ou non créer une balise "Span" dans la structure du document pour exporter la langue du texte.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

### Remarques

La valeur par défaut est`faux` et l'attribut "Lang" est attaché à une séquence de contenu marqué dans un flux de contenu de page.

Lorsque la valeur est`vrai` La balise "Span" est créée pour le texte avec un language autre que celui par défaut et l'attribut "Lang" est attaché à cette balise.

Cette valeur est ignorée lorsque[`ExportDocumentStructure`](../exportdocumentstructure) est`faux` .

### Exemples

Montre comment créer une balise "Span" dans la structure du document pour exporter la langue du texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Notez que lorsque "ExportDocumentStructure" est faux, "ExportLanguageToSpanTag" est ignoré.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../../pdfsaveoptions)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
