---
title: DocumentBase.Lists
linktitle: Lists
articleTitle: Lists
second_title: Aspose.Words pour .NET
description: DocumentBase Lists propriété. Donne accès au formatage de liste utilisé dans le document en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/documentbase/lists/
---
## DocumentBase.Lists property

Donne accès au formatage de liste utilisé dans le document.

```csharp
public ListCollection Lists { get; }
```

## Remarques

Pour plus d'informations, voir la description du[`ListCollection`](../../../aspose.words.lists/listcollection/) classe.

## Exemples

Montre comment utiliser les niveaux de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Vous trouverez ci-dessous deux types de listes que nous pouvons créer à l'aide d'un générateur de documents.
// 1 - Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// En définissant la propriété "ListLevelNumber", nous pouvons augmenter le niveau de la liste
// pour commencer une sous-liste autonome à l'élément de liste actuel.
// Le modèle de liste Microsoft Word appelé « NumberDefault » utilise des nombres pour créer des niveaux de liste pour le premier niveau de liste.
 // Les niveaux de liste plus profonds utilisent des lettres et des chiffres romains minuscules.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Une liste à puces :
// Cette liste appliquera un retrait et une puce ("•") avant chaque paragraphe.
// Les niveaux plus profonds de cette liste utiliseront différents symboles, tels que " ■ " et " ○ ".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Nous pouvons désactiver le formatage de la liste pour ne pas formater les paragraphes suivants sous forme de listes en désactivant l'indicateur "Liste".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Voir également

* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
