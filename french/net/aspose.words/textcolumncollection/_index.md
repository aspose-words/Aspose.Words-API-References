---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: Aspose.Words pour .NET
description: Explorez Aspose.Words.TextColumnCollection pour gérer facilement les colonnes de texte de vos documents. Améliorez facilement la mise en forme de vos documents !
type: docs
weight: 7250
url: /fr/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Une collection de[`TextColumn`](../textcolumn/) objets qui représentent toutes les colonnes de texte dans une section d'un document.

Pour en savoir plus, visitez le[Travailler avec des sections](https://docs.aspose.com/words/net/working-with-sections/) article de documentation.

```csharp
public class TextColumnCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Obtient le nombre de colonnes dans la section d'un document. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Vrai si les colonnes de texte sont de largeur égale et régulièrement espacées. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Renvoie une colonne de texte à l'index spécifié. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Quand`vrai` , ajoute une ligne verticale entre les colonnes. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Lorsque les colonnes sont régulièrement espacées, obtient ou définit la quantité d'espace entre chaque colonne en points. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Lorsque les colonnes sont régulièrement espacées, obtient la largeur des colonnes. |

## Méthodes

| Nom | La description |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | Organise le texte dans le nombre spécifié de colonnes de texte. |

## Remarques

Utiliser[`SetCount`](./setcount/) pour définir le nombre de colonnes de texte.

Pour que toutes les colonnes aient la même largeur et soient espacées uniformément, définissez[`EvenlySpaced`](./evenlyspaced/) à`vrai` et spécifiez la quantité d'espace entre les colonnes dans[`Spacing`](./spacing/). MS Word calculera automatiquement la largeur des colonnes.

Si vous avez[`EvenlySpaced`](./evenlyspaced/) réglé sur`FAUX` Vous devez spécifier la largeur et l'espacement de chaque colonne individuellement. Utilisez l'indexeur pour accéder à chaque colonne.[`TextColumn`](../textcolumn/) objets.

Lorsque vous utilisez des largeurs de colonnes personnalisées, assurez-vous que la somme de toutes les largeurs de colonnes et des espacements entre elles est égale à la largeur de la page moins les marges de page gauche et droite.

## Exemples

Montre comment créer plusieurs colonnes régulièrement espacées dans une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
