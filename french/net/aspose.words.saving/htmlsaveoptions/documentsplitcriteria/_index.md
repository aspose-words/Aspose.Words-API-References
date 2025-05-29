---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HtmlSaveOptions DocumentSplitCriteria pour optimiser l'enregistrement de vos documents aux formats HTML, EPUB et AZW3. Améliorez votre contrôle de mise en forme dès aujourd'hui !
type: docs
weight: 80
url: /fr/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Spécifie comment le document doit être divisé lors de l'enregistrement dansHtml , Epub ouAzw3 format. La valeur par défaut estNone pour HTML et HeadingParagraph pour EPUB et AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Remarques

Normalement, vous voudriez qu'un document soit enregistré au format HTML sous la forme d'un seul fichier. Mais dans certains cas, il est préférable de diviser la sortie en plusieurs pages HTML plus petites. Lors de l'enregistrement au format HTML, ces pages seront exportées vers des fichiers ou des flux individuels. Lors de l'enregistrement au format EPUB, elles seront incorporées dans les packages correspondants.

Un document ne peut pas être divisé lors de l'enregistrement au format MHTML.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
