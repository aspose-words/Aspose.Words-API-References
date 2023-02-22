---
title: HtmlSaveOptions.DocumentSplitCriteria
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Spécifie comment le document doit être divisé lors de lenregistrement dansHtml ouEpub format. La valeur par défaut estNone pour HTML et HeadingParagraph pour EPUB.
type: docs
weight: 80
url: /fr/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Spécifie comment le document doit être divisé lors de l'enregistrement dansHtml ouEpub format. La valeur par défaut estNone pour HTML et HeadingParagraph pour EPUB.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

### Remarques

Normalement, vous voudriez qu'un document soit enregistré au format HTML en tant que fichier unique. Mais dans certains cas, il est préférable de diviser la sortie en plusieurs pages HTML plus petites. Lors de l'enregistrement au format HTML, ces pages seront sorties dans des fichiers ou des flux individuels. Lors de l'enregistrement au format EPUB, ils seront incorporés dans les packages correspondants.

Un document ne peut pas être divisé lors de l'enregistrement au format MHTML.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


