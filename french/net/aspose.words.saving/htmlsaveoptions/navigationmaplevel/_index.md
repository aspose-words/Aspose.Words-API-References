---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words pour .NET
description: Découvrez la propriété NavigationMapLevel de HtmlSaveOptions, qui contrôle les niveaux de titre pour les exportations EPUB, MOBI et AZW3. Optimisez la visibilité de votre contenu !
type: docs
weight: 390
url: /fr/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Spécifie le niveau maximal de titres renseignés dans la carte de navigation lors de l'exportation aux formats EPUB, MOBI ou AZW3 . La valeur par défaut est`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Remarques

La carte de navigation permet aux agents utilisateurs de naviguer facilement dans la structure du document. Généralement, les points de navigation correspondent aux titres du document. Pour renseigner les titres jusqu'au niveau**N** attribuez cette valeur à`NavigationMapLevel`.

Par défaut, trois niveaux de titres sont renseignés : paragraphes de styles**Titre 1** ,**Titre 2** et**Titre 3**. Vous pouvez définir cette propriété sur une valeur de 1 à 9 afin de demander le niveau maximum correspondant. La définir sur zéro réduira la carte de navigation uniquement à la racine du document ou aux racines des parties du document.

## Exemples

Montre comment générer une table des matières pour les documents Azw3.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

Montre comment générer une table des matières pour les documents Mobi.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

Montre comment filtrer les titres qui apparaissent dans le panneau de navigation d'un document Epub enregistré.

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

// Les lecteurs Epub créent généralement une table des matières pour leurs documents.
// Chaque paragraphe avec un style « Titre » dans le document créera une entrée dans cette table des matières.
 // Nous pouvons utiliser la propriété « NavigationMapLevel » pour définir un niveau de cap maximal.
// Le lecteur Epub n'ajoutera pas de titres avec un niveau supérieur à celui que nous spécifions à la table des matières.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

// Notre document comporte six titres, dont deux sont au-dessus du niveau 2.
// La table des matières de ce document comportera quatre entrées.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
