---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words pour .NET
description: Découvrez comment Aspose.Words.Saving.DocumentSplitCriteria optimise le fractionnement des documents pour des formats HTML, EPUB et AZW3 optimaux. Simplifiez votre processus de sauvegarde !
type: docs
weight: 5710
url: /fr/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Spécifie comment le document est divisé en parties lors de l'enregistrement dansHtml , Epub ouAzw3 format.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Le document n'est pas divisé. |
| PageBreak | `1` | Le document est divisé en parties avec des sauts de page explicites. Un saut de page peut être spécifié par un[`PageBreak`](../../aspose.words/controlchar/pagebreak/) caractère, un saut de section spécifiant le début d'une nouvelle section sur une nouvelle page, ou un paragraphe qui a son[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) propriété définie sur`vrai` . |
| ColumnBreak | `2` | Le document est divisé en parties aux sauts de colonne. Un saut de colonne peut être spécifié par un[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) caractère ou un saut de section spécifiant le début d'une nouvelle section dans une nouvelle colonne. |
| SectionBreak | `4` | Le document est divisé en parties lors d'un saut de section de n'importe quel type. |
| HeadingParagraph | `8` | Le document est divisé en parties dans un paragraphe formaté à l'aide d'un style de titre**Titre 1** ,**Titre 2** etc. À utiliser avec[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) pour spécifier les niveaux de titre (de 1 au niveau spécifié) auxquels fractionner. |

## Remarques

`DocumentSplitCriteria`Il s'agit d'un ensemble d'indicateurs combinables. Par exemple, vous pouvez scinder le document au niveau des sauts de page et des paragraphes d'en-tête lors de la même opération d'exportation.

Différents critères peuvent se chevaucher partiellement. Par exemple,**Titre 1** le style est souvent donné [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) propriété, elle répond donc à deux critères :PageBreak et HeadingParagraph. Certains sauts de section peuvent provoquer des sauts de page, etc. Dans les cas typiques, spécifier un seul indicateur est l'option la plus pratique.

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
