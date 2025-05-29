---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words pour .NET
description: Maîtrisez la mise en forme des listes dans vos documents avec la classe Aspose.Words.Lists.ListFormat. Améliorez facilement le style des paragraphes pour une meilleure lisibilité.
type: docs
weight: 3930
url: /fr/net/aspose.words.lists/listformat/
---
## ListFormat class

Permet de contrôler la mise en forme de liste appliquée à un paragraphe.

Pour en savoir plus, visitez le[Travailler avec des listes](https://docs.aspose.com/words/net/working-with-lists/) article de documentation.

```csharp
public class ListFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Vrai lorsque le paragraphe est doté d'une mise en forme à puces ou numérotée. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Obtient ou définit la liste dont ce paragraphe est membre. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Renvoie la mise en forme au niveau de la liste ainsi que toutes les substitutions de mise en forme appliquées au paragraphe actuel. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Obtient ou définit le numéro de niveau de liste (0 à 8) pour le paragraphe. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Démarre une nouvelle liste à puces par défaut et l'applique au paragraphe. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Démarre une nouvelle liste numérotée par défaut et l'applique au paragraphe. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Augmente le niveau de liste du paragraphe actuel d'un niveau. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Diminue le niveau de liste du paragraphe actuel d'un niveau. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Supprime les numéros ou les puces du paragraphe actuel et définit le niveau de la liste à zéro. |

## Remarques

Un paragraphe dans un document Microsoft Word peut être à puces ou numéroté. Lorsqu'un paragraphe est à puces ou numéroté, on dit que la mise en forme de liste est appliquée au paragraphe.

Vous ne créez pas d'objets de la`ListFormat` classe directement. Vous accédez`ListFormat`comme propriété d'un autre objet auquel un formatage de liste peut être associé. Actuellement, les objets pouvant être formatés de liste sont :[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) et[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` d'un[`Paragraph`](../../aspose.words/paragraph/) spécifie quel formatage de liste et quel niveau de liste sont appliqués à ce paragraphe particulier.

`ListFormat` d'un[`Style`](../../aspose.words/style/) (applicable aux styles de paragraphe uniquement) permet de spécifier quel formatage de liste et quel niveau de liste sont appliqués à tous les paragraphes de ce style particulier.

`ListFormat` d'un[`DocumentBuilder`](../../aspose.words/documentbuilder/) permet d'accéder au formatage de la liste à la position actuelle du curseur à l'intérieur du[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Le formatage de la liste elle-même est stocké dans un[`List`](../list/) Objet stocké séparément des paragraphes. Les objets de liste sont stockés dans un[`ListCollection`](../listcollection/) collection. Il y a un single [`ListCollection`](../listcollection/) collecte par[`Document`](../../aspose.words/document/).

Les paragraphes n'appartiennent pas physiquement à une liste. Ils font simplement référence à un objet de liste particulier via le[`List`](./list/) property et un niveau particulier dans la liste via le[`ListLevelNumber`](./listlevelnumber/) property. En définissant ces deux propriétés, vous contrôlez les puces et la numérotation qui sont appliquées à un paragraphe.

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

### Voir également

* espace de noms [Aspose.Words.Lists](../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../)
