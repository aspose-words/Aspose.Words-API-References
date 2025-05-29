---
title: HtmlSaveOptions.ExportDocumentProperties
linktitle: ExportDocumentProperties
articleTitle: ExportDocumentProperties
second_title: Aspose.Words pour .NET
description: Découvrez comment ExportDocumentProperties de HtmlSaveOptions améliore vos exportations HTML, MHTML ou EPUB en incluant des propriétés de document intégrées et personnalisées essentielles.
type: docs
weight: 120
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Spécifie s'il faut exporter les propriétés de document intégrées et personnalisées vers HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool ExportDocumentProperties { get; set; }
```

## Exemples

Montre comment utiliser un codage spécifique lors de l'enregistrement d'un document au format .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilisez un objet SaveOptions pour spécifier l'encodage d'un document que nous allons enregistrer.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Par défaut, un document .epub de sortie aura tout son contenu dans une seule partie HTML.
// Un critère de division nous permet de segmenter le document en plusieurs parties HTML.
// Nous allons définir les critères pour diviser le document en paragraphes d'en-tête.
// Ceci est utile pour les lecteurs qui ne peuvent pas lire les fichiers HTML plus importants qu'une taille spécifique.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Spécifiez que nous voulons exporter les propriétés du document.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
