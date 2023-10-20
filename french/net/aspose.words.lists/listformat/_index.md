---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words pour .NET
description: Aspose.Words.Lists.ListFormat classe. Permet de contrôler quel formatage de liste est appliqué à un paragraphe en C#.
type: docs
weight: 3480
url: /fr/net/aspose.words.lists/listformat/
---
## ListFormat class

Permet de contrôler quel formatage de liste est appliqué à un paragraphe.

Pour en savoir plus, visitez le[Travailler avec des listes](https://docs.aspose.com/words/net/working-with-lists/) article documentaire.

```csharp
public class ListFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Vrai lorsque le paragraphe est doté d'une mise en forme de puces ou de numéros. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Obtient ou définit la liste dont ce paragraphe est membre. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Renvoie le formatage au niveau de la liste ainsi que tout remplacement de formatage appliqué au paragraphe actuel. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Obtient ou définit le numéro de niveau de liste (0 à 8) pour le paragraphe. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Démarre une nouvelle liste à puces par défaut et l'applique au paragraphe. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Démarre une nouvelle liste numérotée par défaut et l'applique au paragraphe. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Augmente le niveau de liste du paragraphe actuel d'un niveau. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Diminue le niveau de liste du paragraphe actuel d'un niveau. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Supprime les chiffres ou les puces du paragraphe actuel et définit le niveau de liste sur zéro. |

## Remarques

Un paragraphe dans un document Microsoft Word peut être à puces ou numéroté. Lorsqu'un paragraphe est à puces ou numéroté, on dit que le formatage de liste est appliqué au paragraphe.

Vous ne créez pas d'objets du`ListFormat` classe directement. Vous accédez`ListFormat` en tant que propriété d'un autre objet auquel can est associé à un formatage de liste. Pour le moment, les objets qui can ont un format de liste sont :[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) et[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` d'un[`Paragraph`](../../aspose.words/paragraph/) spécifie quel formatage de liste et quel niveau de liste sont appliqués à ce paragraphe particulier.

`ListFormat` d'un[`Style`](../../aspose.words/style/) (applicable aux styles de paragraphe uniquement) permet de spécifier quel formatage de liste et quel niveau de liste est appliqué à tous les paragraphes de ce style particulier.

`ListFormat` d'un[`DocumentBuilder`](../../aspose.words/documentbuilder/) donne accès au formatage de la liste à la position actuelle du curseur à l'intérieur du[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Le formatage de la liste lui-même est stocké dans un[`List`](../list/) Objet qui est stocké séparément des paragraphes. La liste object est stockée dans un[`ListCollection`](../listcollection/) collection. Il existe un single [`ListCollection`](../listcollection/) collecte par[`Document`](../../aspose.words/document/).

Les paragraphes n'appartiennent pas physiquement à une liste. Les paragraphes just font référence à un objet de liste particulier via le[`List`](./list/) property et un niveau particulier dans la liste via le[`ListLevelNumber`](./listlevelnumber/) property. En définissant ces deux propriétés, vous contrôlez quelles puces et quelle numérotation sont appliquées à un paragraphe.

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

* espace de noms [Aspose.Words.Lists](../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../)
