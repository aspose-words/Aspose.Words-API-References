---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words pour .NET
description: Optimisez le fractionnement des documents avec DocumentSplitHeadingLevel de HtmlSaveOptions. Contrôlez les niveaux de titre pour une meilleure organisation. La valeur par défaut est 2.
type: docs
weight: 90
url: /fr/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Spécifie le niveau maximal de titres auquel diviser le document. La valeur par défaut est`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## Remarques

Quand[`DocumentSplitCriteria`](../documentsplitcriteria/) comprendHeadingParagraph et cette propriété est définie sur une valeur de 1 à 9, le document sera divisé en paragraphes formatés à l'aide de **Titre 1** ,**Titre 2** ,**Titre 3**etc. styles jusqu'au niveau de titre spécifié.

Par défaut, seulement**Titre 1** et**Titre 2** les paragraphes provoquent la division du document. La définition de cette propriété sur zéro entraînera la non-division du document au niveau des paragraphes d'en-tête.

## Exemples

Montre comment diviser un document HTML de sortie par titres en plusieurs parties.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Chaque paragraphe que nous formatons à l'aide d'un style « Titre » peut servir de titre.
// Chaque titre peut également avoir un niveau de titre, déterminé par le numéro de son style de titre.
// Les titres ci-dessous sont de niveaux 1 à 3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Créez un objet HtmlSaveOptions et définissez les critères de division sur « HeadingParagraph ».
// Ces critères diviseront le document en paragraphes avec des styles « Titre » en plusieurs documents plus petits,
// et enregistrez chaque document dans un fichier HTML séparé dans le système de fichiers local.
// Nous allons également définir le niveau de titre maximum, qui divise le document en 2.
// L'enregistrement du document le divisera en titres de niveaux 1 et 2, mais pas de 3 à 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Notre document comporte quatre titres de niveaux 1 à 2. L'un de ces titres ne sera pas
// un point de division puisqu'il se trouve au début du document.
// L'opération de sauvegarde divisera notre document en trois endroits, en quatre documents plus petits.
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
