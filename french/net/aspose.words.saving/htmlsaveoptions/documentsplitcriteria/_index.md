---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions DocumentSplitCriteria propriété. Spécifie comment le document doit être divisé lors de lenregistrement surHtml  Epub ouAzw3 format. La valeur par défaut estNone pour HTML et HeadingParagraph pour EPUB et AZW3 en C#.
type: docs
weight: 80
url: /fr/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Spécifie comment le document doit être divisé lors de l'enregistrement surHtml , Epub ouAzw3 format. La valeur par défaut estNone pour HTML et HeadingParagraph pour EPUB et AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Remarques

Normalement, vous souhaiteriez qu’un document soit enregistré au format HTML sous forme de fichier unique. Mais dans certains cas, il est préférable de diviser la sortie en plusieurs pages HTML plus petites. Lors de l'enregistrement au format HTML, ces pages seront sorties dans des fichiers ou des flux individuels. Lors de l'enregistrement au format EPUB, ils seront incorporés dans les packages correspondants.

Un document ne peut pas être fractionné lors de son enregistrement au format MHTML.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
