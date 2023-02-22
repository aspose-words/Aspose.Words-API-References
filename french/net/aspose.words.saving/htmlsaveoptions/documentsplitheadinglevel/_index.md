---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Spécifie le niveau maximal dentêtes auquel diviser le document. La valeur par défaut est2 .
type: docs
weight: 90
url: /fr/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Spécifie le niveau maximal d'en-têtes auquel diviser le document. La valeur par défaut est`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

### Remarques

Lorsque[`DocumentSplitCriteria`](../documentsplitcriteria/) comprendHeadingParagraph et que cette propriété est définie sur une valeur comprise entre 1 et 9, le document sera divisé en paragraphes formatés à l'aide de  **Rubrique 1** , **Rubrique 2** , **Rubrique 3** etc. styles jusqu'au niveau de titre spécifié.

Par défaut, uniquement **Rubrique 1** et **Rubrique 2** les paragraphes provoquent le fractionnement du document. Si vous définissez cette propriété sur zéro, le document ne sera pas du tout divisé au niveau des paragraphes d'en-tête.

### Exemples

Montre comment diviser un document HTML de sortie par en-têtes en plusieurs parties.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Chaque paragraphe que nous formatons en utilisant un style "Titre" peut servir de titre.
// Chaque titre peut également avoir un niveau de titre, déterminé par le numéro de son style de titre.
// Les titres ci-dessous sont des niveaux 1-3.
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

// Crée un objet HtmlSaveOptions et définit le critère de fractionnement sur "HeadingParagraph".
// Ces critères diviseront le document au niveau des paragraphes avec des styles "Titre" en plusieurs documents plus petits,
// et enregistrez chaque document dans un fichier HTML séparé dans le système de fichiers local.
// Nous définirons également le niveau d'en-tête maximum, qui divise le document en 2.
// L'enregistrement du document le divisera aux en-têtes de niveaux 1 et 2, mais pas aux niveaux 3 à 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Notre document comporte quatre rubriques de niveaux 1 - 2. L'une de ces rubriques ne sera pas
// un point de partage puisqu'il se trouve au début du document.
// L'opération d'enregistrement divisera notre document à trois endroits, en quatre documents plus petits.
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
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


