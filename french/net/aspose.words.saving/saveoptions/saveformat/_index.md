---
title: SaveOptions.SaveFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Spécifie le format dans lequel le document sera enregistré si cet objet doptions denregistrement est utilisé.
type: docs
weight: 140
url: /fr/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé.

```csharp
public abstract SaveFormat SaveFormat { get; set; }
```

### Exemples

Montre comment utiliser un encodage spécifique lors de l'enregistrement d'un document au format .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilisez un objet SaveOptions pour spécifier l'encodage d'un document que nous allons enregistrer.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Par défaut, un document de sortie .epub aura tout son contenu dans une seule partie HTML.
// Un critère de découpage permet de segmenter le document en plusieurs parties HTML.
// Nous allons définir les critères pour diviser le document en paragraphes d'en-tête.
// Ceci est utile pour les lecteurs qui ne peuvent pas lire les fichiers HTML plus importants qu'une taille spécifique.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Spécifiez que nous voulons exporter les propriétés du document.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


