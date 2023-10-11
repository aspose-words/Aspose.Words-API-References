---
title: Enum ListTemplate
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Lists.ListTemplate énumération. Spécifie lun des formats de liste prédéfinis disponibles dans Microsoft Word.
type: docs
weight: 3530
url: /fr/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Spécifie l'un des formats de liste prédéfinis disponibles dans Microsoft Word.

```csharp
public enum ListTemplate
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| BulletDefault | `0` | Liste à puces par défaut avec 9 niveaux. La balle du premier niveau est un disque, la balle du deuxième niveau est un cercle, la balle du troisième niveau est un carré. Ensuite, le formatage se répète pour les niveaux restants. |
| BulletDisk | `0` | Pareil queBulletDefault. |
| BulletCircle | `1` | La puce du premier niveau est un cercle. Les niveaux restants sont les mêmes que dansBulletDefault. |
| BulletSquare | `2` | La puce du premier niveau est un carré. Les niveaux restants sont les mêmes que dansBulletDefault. |
| BulletDiamonds | `3` | La balle du premier niveau est un personnage Wingding à 4 diamants. Les niveaux restants sont les mêmes que dansBulletDefault. |
| BulletArrowHead | `4` | La balle du premier niveau est un personnage Wingding à tête de flèche. Les niveaux restants sont les mêmes que dansBulletDefault. |
| BulletTick | `5` | La balle du premier niveau est un personnage de tick Wingding. Les niveaux restants sont les mêmes que dansBulletDefault. |
| NumberDefault | `6` | Liste numérotée par défaut avec 9 niveaux. Numérotation arabe (1., 2., 3., ...) pour le premier niveau, numérotation des lettres minuscules (a., b., c., ...) pour le deuxième niveau, numérotation romaine minuscule (i ., ii., iii., ...) pour le troisième niveau. Puis le formatage se répète pour les niveaux restants. |
| NumberArabicDot | `6` | Pareil queNumberDefault. |
| NumberArabicParenthesis | `7` | Le numéro du premier niveau est "1)". Les niveaux restants sont les mêmes que dansNumberDefault. |
| NumberUppercaseRomanDot | `8` | Le numéro du premier niveau est "I". Les niveaux restants sont les mêmes que dansNumberDefault. |
| NumberUppercaseLetterDot | `9` | Le numéro du premier niveau est « A ». Les niveaux restants sont les mêmes que dansNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Le numéro du premier niveau est "a)". Les niveaux restants sont les mêmes que dansNumberDefault. |
| NumberLowercaseLetterDot | `11` | Le numéro du premier niveau est "a". Les niveaux restants sont les mêmes que dansNumberDefault. |
| NumberLowercaseRomanDot | `12` | Le numéro du premier niveau est "i". Les niveaux restants sont les mêmes que dansNumberDefault. |
| OutlineNumbers | `13` | Une liste schématique avec des niveaux numérotés "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | Une liste schématique avec des niveaux numérotés "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | Un plan répertorie différentes puces pour différents niveaux. |
| OutlineHeadingsArticleSection | `16` | Une liste hiérarchique avec des niveaux liés aux styles de titre. |
| OutlineHeadingsLegal | `17` | Une liste hiérarchique avec des niveaux liés aux styles de titre. |
| OutlineHeadingsNumbers | `18` | Une liste hiérarchique avec des niveaux liés aux styles de titre. |
| OutlineHeadingsChapter | `19` | Une liste hiérarchique avec des niveaux liés aux styles de titre. |

### Remarques

Une valeur de modèle de liste est utilisée comme paramètre dans the [`Add`](../listcollection/add/) méthode.

Les modèles de liste Aspose.Words correspondent aux 21 modèles de liste disponibles dans la boîte de dialogue Puces et numérotation de Microsoft Word 2003.

### Exemples

Montre comment créer un document contenant tous les modèles de liste de titres hiérarchiques.

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

Montre comment redémarrer la numérotation dans une liste en copiant une liste.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste à partir d'un modèle Microsoft Word et personnalisez son premier niveau de liste.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Applique notre liste à certains paragraphes.
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

// Applique la deuxième liste aux nouveaux paragraphes.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

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


