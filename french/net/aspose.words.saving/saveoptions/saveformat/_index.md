---
title: SaveOptions.SaveFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Spécifie le format dans lequel le document sera enregistré si cet objet doptions de sauvegarde est utilisé.
type: docs
weight: 130
url: /fr/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options de sauvegarde est utilisé.

```csharp
public abstract SaveFormat SaveFormat { get; set; }
```

### Exemples

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


