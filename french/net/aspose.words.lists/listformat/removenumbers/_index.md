---
title: ListFormat.RemoveNumbers
linktitle: RemoveNumbers
articleTitle: RemoveNumbers
second_title: Aspose.Words pour .NET
description: ListFormat RemoveNumbers méthode. Supprime les chiffres ou les puces du paragraphe actuel et définit le niveau de liste sur zéro en C#.
type: docs
weight: 90
url: /fr/net/aspose.words.lists/listformat/removenumbers/
---
## ListFormat.RemoveNumbers method

Supprime les chiffres ou les puces du paragraphe actuel et définit le niveau de liste sur zéro.

```csharp
public void RemoveNumbers()
```

## Remarques

Appeler cette méthode équivaut à définir le[`List`](../list/) propriété à`nul`.

## Exemples

Montre comment supprimer la mise en forme de liste de tous les paragraphes du texte principal d’une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);
Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

foreach (Paragraph paragraph in paras)
    paragraph.ListFormat.RemoveNumbers();

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
```

Montre comment créer des listes à puces et numérotées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Vous trouverez ci-dessous deux types de listes que nous pouvons créer avec un générateur de documents.
// 1 - Une liste à puces :
// Cette liste appliquera un retrait et une puce ("•") avant chaque paragraphe.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Termine la liste à puces.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder.ListFormat.ApplyNumberDefault();

// Ce paragraphe est le premier élément. Le premier élément d'une liste numérotée aura un « 1 ». comme symbole d'élément de liste.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Appel de la méthode "ListIndent" pour augmenter le niveau courant de la liste,
// qui démarrera une nouvelle liste autonome, avec un retrait plus profond, à l'élément actuel du premier niveau de liste.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Ce sont les trois premiers éléments de liste du deuxième niveau de liste, qui maintiendront un décompte
// indépendant du nombre du premier niveau de liste. Selon le format de liste actuel,
// ils auront les symboles "a.", "b." et "c."
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Appelez la méthode "ListOutdent" pour revenir au niveau de liste précédent.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Ces deux paragraphes continueront le décompte du premier niveau de liste.
// Ces éléments auront les symboles "2." et "3".
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Si nous augmentons le niveau de la liste à un niveau auquel nous avons ajouté des éléments précédemment,
 // la liste imbriquée sera distincte de la précédente et sa numérotation recommencera depuis le début.
// Ces éléments de liste auront les symboles "a.", "b.", "c.", "d." et "e".
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Dépasse à nouveau le niveau de la liste.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Termine la liste numérotée.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Voir également

* class [ListFormat](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
