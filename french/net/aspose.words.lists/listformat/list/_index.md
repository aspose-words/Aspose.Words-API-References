---
title: ListFormat.List
linktitle: List
articleTitle: List
second_title: Aspose.Words pour .NET
description: Gérez la structure de votre document avec ListFormat. Obtenez ou définissez facilement la liste de chaque paragraphe, améliorant ainsi son organisation et sa lisibilité.
type: docs
weight: 20
url: /fr/net/aspose.words.lists/listformat/list/
---
## ListFormat.List property

Obtient ou définit la liste dont ce paragraphe est membre.

```csharp
public List List { get; set; }
```

## Remarques

La liste qui est attribuée à cette propriété doit appartenir au document actuel.

La liste qui est attribuée à cette propriété ne doit pas être une définition de style de liste.

Définir cette propriété sur`nul` supprime les puces et la numérotation du paragraphe et définit le numéro de niveau de liste à zéro. Définir cette propriété sur`nul` est equivalent à appeler[`RemoveNumbers`](../removenumbers/).

## Exemples

Montre comment imbriquer une liste dans une autre liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété « ListFormat » d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste de contours pour les titres.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Créer une liste numérotée.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Chaque paragraphe qui comprend une liste aura cet indicateur.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Créer une liste à puces.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Revenir à la liste numérotée.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Revenir à la liste des contours.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

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

### Voir également

* class [List](../../list/)
* class [ListFormat](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
