---
title: ListFormat.ListLevelNumber
linktitle: ListLevelNumber
articleTitle: ListLevelNumber
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ListFormat ListLevelNumber, gérez facilement les niveaux de liste de paragraphes de 0 à 8 pour une organisation et une clarté améliorées du document.
type: docs
weight: 40
url: /fr/net/aspose.words.lists/listformat/listlevelnumber/
---
## ListFormat.ListLevelNumber property

Obtient ou définit le numéro de niveau de liste (0 à 8) pour le paragraphe.

```csharp
public int ListLevelNumber { get; set; }
```

## Remarques

Dans les documents Word, les listes peuvent être composées de 1 ou 9 niveaux, numérotés de 0 à 8.

N'a d'effet que lorsque le[`List`](../list/) la propriété est définie pour référencer une liste valide.

## Exemples

Montre comment travailler avec les niveaux de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété « ListFormat » d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Vous trouverez ci-dessous deux types de listes que nous pouvons créer à l’aide d’un générateur de documents.
// 1 - Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// En définissant la propriété « ListLevelNumber », nous pouvons augmenter le niveau de la liste
// pour commencer une sous-liste autonome à partir de l'élément de liste actuel.
// Le modèle de liste Microsoft Word appelé « NumberDefault » utilise des nombres pour créer des niveaux de liste pour le premier niveau de liste.
 // Les niveaux de liste plus profonds utilisent des lettres et des chiffres romains minuscules.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Une liste à puces :
// Cette liste appliquera un retrait et un symbole de puce (« • ») avant chaque paragraphe.
// Les niveaux plus profonds de cette liste utiliseront des symboles différents, tels que « ■ » et « ○ ».
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Nous pouvons désactiver le formatage de liste pour ne pas formater les paragraphes suivants sous forme de listes en désactivant l'indicateur « Liste ».
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

Montre comment créer des listes à puces et numérotées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété « ListFormat » d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Vous trouverez ci-dessous deux types de listes que nous pouvons créer avec un générateur de documents.
// 1 - Une liste à puces :
// Cette liste appliquera un retrait et un symbole de puce (« • ») avant chaque paragraphe.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Terminer la liste à puces.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder.ListFormat.ApplyNumberDefault();

// Ce paragraphe est le premier élément. Le premier élément d'une liste numérotée aura « 1. » comme symbole.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Appelez la méthode "ListIndent" pour augmenter le niveau de liste actuel,
// qui démarrera une nouvelle liste autonome, avec un retrait plus profond, à l'élément actuel du premier niveau de liste.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Ce sont les trois premiers éléments de la liste du deuxième niveau de liste, qui conserveront un compte
// indépendant du nombre de niveaux de la liste. Selon le format de liste actuel,
// ils auront des symboles de « a. », « b. » et « c. ».
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Appelez la méthode « ListOutdent » pour revenir au niveau de liste précédent.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Ces deux paragraphes continueront le décompte du premier niveau de liste.
// Ces éléments auront les symboles « 2 » et « 3 ».
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Si nous augmentons le niveau de la liste à un niveau auquel nous avons ajouté des éléments précédemment,
 // la liste imbriquée sera séparée de la précédente et sa numérotation commencera depuis le début.
// Ces éléments de liste auront les symboles « a. », « b. », « c. », « d. » et « e ».
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Augmentez à nouveau le niveau de la liste.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Terminer la liste numérotée.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Voir également

* class [ListFormat](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
