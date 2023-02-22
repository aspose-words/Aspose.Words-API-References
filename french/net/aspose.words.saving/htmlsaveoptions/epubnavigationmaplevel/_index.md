---
title: HtmlSaveOptions.EpubNavigationMapLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Spécifie le niveau maximal dentêtes remplis dans la carte de navigation lors de lexportation au format IDPF EPUB. La valeur par défaut est3 .
type: docs
weight: 110
url: /fr/net/aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/
---
## HtmlSaveOptions.EpubNavigationMapLevel property

Spécifie le niveau maximal d'en-têtes remplis dans la carte de navigation lors de l'exportation au format IDPF EPUB. La valeur par défaut est`3` .

```csharp
public int EpubNavigationMapLevel { get; set; }
```

### Remarques

La carte de navigation au format IDPF EPUB permet aux agents utilisateurs de faciliter la navigation dans la structure du document. Généralement, les points de navigation correspondent aux en-têtes du document. Pour remplir les en-têtes jusqu'au niveau **N** attribuer cette valeur à`EpubNavigationMapLevel`.

Par défaut, trois niveaux de titres sont renseignés : paragraphes de styles **Rubrique 1** , **Rubrique 2** et **Rubrique 3**. Vous pouvez définir cette propriété sur une valeur comprise entre 1 et 9 pour demander le niveau maximum correspondant. Le mettre à zéro réduira la carte de navigation uniquement à la racine du document ou aux racines des parties du document.

### Exemples

Montre comment filtrer les titres qui apparaissent dans le panneau de navigation d'un document Epub enregistré.

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

// Les lecteurs d'Epub créent généralement une table des matières pour leurs documents.
// Chaque paragraphe avec un style "Titre" dans le document créera une entrée dans cette table des matières.
 // Nous pouvons utiliser la propriété "EpubNavigationMapLevel" pour définir un niveau d'en-tête maximum.
// Le lecteur Epub n'ajoutera pas de titres avec un niveau supérieur à celui que nous spécifions à la table des matières.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.EpubNavigationMapLevel = 2;

// Notre document comporte six rubriques, dont deux sont au-dessus du niveau 2.
// La table des matières de ce document aura quatre entrées.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


