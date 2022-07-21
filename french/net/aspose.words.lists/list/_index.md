---
title: List
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente le formatage dune liste.
type: docs
weight: 3260
url: /fr/net/aspose.words.lists/list/
---
## List class

Représente le formatage d'une liste.

```csharp
public class List : IComparable<List>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Document](../../aspose.words.lists/list/document) { get; } | Obtient le document propriétaire. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition) { get; } | Renvoie true si cette liste est une définition d'un style de liste. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference) { get; } | Renvoie vrai si cette liste est une référence à un style de liste. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel) { get; } | Renvoie true lorsque la liste contient 9 niveaux ; faux quand 1 niveau. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection) { get; set; } | Spécifie si la liste doit être redémarrée à chaque section. La valeur par défaut est **faux** . |
| [ListId](../../aspose.words.lists/list/listid) { get; } | Obtient l'identifiant unique de la liste. |
| [ListLevels](../../aspose.words.lists/list/listlevels) { get; } | Obtient la collection de niveaux de liste pour cette liste. |
| [Style](../../aspose.words.lists/list/style) { get; } | Obtient le style de liste auquel cette liste fait référence ou définit. |

## Méthodes

| Nom | La description |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto#compareto)(List) | Compare la liste spécifiée à la liste actuelle. |
| [CompareTo](../../aspose.words.lists/list/compareto#compareto_1)(object) | Compare l'objet spécifié à l'objet actuel. |
| [Equals](../../aspose.words.lists/list/equals#equals)(List) | Compare avec la liste spécifiée. |
| override [Equals](../../aspose.words.lists/list/equals#equals_1)(object) |  |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode)() | Calcule le code de hachage pour cet objet de liste. |

### Remarques

Une liste dans un document Microsoft Word est un ensemble de propriétés de formatage de liste. Chaque liste peut avoir jusqu'à 9 niveaux et les propriétés de formatage, telles que le style de nombre, la valeur de départ, le retrait , la position des tabulations, etc. sont définies séparément pour chaque niveau.

UN[`List`](../list) l'objet appartient toujours au[`ListCollection`](../listcollection) le recueil.

Pour créer une nouvelle liste, utilisez les méthodes Add de la[`ListCollection`](../listcollection) le recueil.

Pour modifier la mise en forme d'une liste, utilisez[`ListLevel`](../listlevel) objets trouvés dans le[`ListLevels`](./listlevels) le recueil.

Pour appliquer ou supprimer la mise en forme de liste d'un paragraphe, utilisez[`ListFormat`](../listformat).

### Exemples

Montre comment redémarrer la numérotation dans une liste en copiant une liste.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation. 
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de document. 
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Crée une liste à partir d'un modèle Microsoft Word et personnalise son premier niveau de liste.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Appliquez notre liste à certains paragraphes.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Nous pouvons ajouter une copie d'une liste existante à la collection de listes du document
// pour créer une liste similaire sans apporter de modifications à l'original.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Applique la seconde liste aux nouveaux paragraphes.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Montre comment appliquer une mise en forme de liste personnalisée aux paragraphes lors de l'utilisation de DocumentBuilder.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation. 
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de document. 
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Crée une liste à partir d'un modèle Microsoft Word et personnalise les deux premiers de ses niveaux de liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Cette valeur NumberFormat créera des symboles de liste à puces en forme d'étoile.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Créez des paragraphes et appliquez-leur les deux niveaux de liste de notre formatage de liste personnalisé.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

Montre comment travailler avec les niveaux de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation. 
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de document. 
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Vous trouverez ci-dessous deux types de listes que nous pouvons créer à l'aide d'un générateur de documents.
// 1 - Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// En définissant la propriété "ListLevelNumber", nous pouvons augmenter le niveau de la liste
// pour commencer une sous-liste autonome à l'élément de liste actuel.
// Le modèle de liste Microsoft Word appelé "NumberDefault" utilise des nombres pour créer des niveaux de liste pour le premier niveau de liste.
// Les niveaux de liste plus profonds utilisent des lettres et des chiffres romains minuscules. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Une liste à puces :
// Cette liste appliquera un retrait et un symbole de puce ("•") avant chaque paragraphe.
// Les niveaux plus profonds de cette liste utiliseront différents symboles, tels que "■" et "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Nous pouvons désactiver le formatage de la liste pour ne pas formater les paragraphes suivants en tant que listes en désactivant le drapeau "Liste".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Voir également

* espace de noms [Aspose.Words.Lists](../../aspose.words.lists)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
