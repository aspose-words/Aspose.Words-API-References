---
title: HtmlSaveOptions.ExportDocumentProperties
linktitle: ExportDocumentProperties
articleTitle: ExportDocumentProperties
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ExportDocumentProperties propriété. Spécifie sil faut exporter les propriétés du document intégré et personnalisé au format HTML MHTML ou EPUB. La valeur par défaut estFAUX  en C#.
type: docs
weight: 120
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Spécifie s'il faut exporter les propriétés du document intégré et personnalisé au format HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool ExportDocumentProperties { get; set; }
```

## Exemples

Montre comment utiliser un encodage spécifique lors de l’enregistrement d’un document au format .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilisez un objet SaveOptions pour spécifier l'encodage d'un document que nous allons enregistrer.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Par défaut, un document de sortie .epub aura tout son contenu dans une seule partie HTML.
// Un critère de split permet de segmenter le document en plusieurs parties HTML.
// Nous définirons les critères pour diviser le document en paragraphes de titre.
// Ceci est utile pour les lecteurs qui ne peuvent pas lire des fichiers HTML d'une taille supérieure à une taille spécifique.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Spécifie que nous souhaitons exporter les propriétés du document.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
