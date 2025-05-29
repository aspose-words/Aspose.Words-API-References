---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Tables.PreferredWidth, votre solution pour définir des largeurs de tableau et de cellule optimales avec précision et flexibilité. Améliorez la mise en page de vos documents dès aujourd'hui !
type: docs
weight: 7140
url: /fr/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Représente une valeur et son unité de mesure qui est utilisée pour spécifier la largeur préférée d'un tableau ou d'une cellule.

Pour en savoir plus, visitez le[Travailler avec des tableaux](https://docs.aspose.com/words/net/working-with-tables/) article de documentation.

```csharp
public sealed class PreferredWidth
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Obtient l'unité de mesure utilisée pour cette valeur de largeur préférée. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Récupère la valeur de largeur préférée. L'unité de mesure est spécifiée dans le[`Type`](./type/) propriété. |

## Méthodes

| Nom | La description |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | Une méthode de création qui renvoie une nouvelle instance qui représente une largeur préférée spécifiée sous forme de pourcentage. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | Une méthode de création qui renvoie une nouvelle instance qui représente une largeur préférée spécifiée à l'aide d'un nombre de points. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | Détermine si le spécifié`PreferredWidth` est égal en valeur au courant`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Sert de fonction de hachage pour ce type. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |

## Des champs

| Nom | La description |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | Renvoie une instance qui représente la valeur « la largeur préférée n'est pas spécifiée ». |

## Remarques

La largeur préférée peut être spécifiée sous forme de pourcentage, de nombre de points ou d'une valeur spéciale « aucune/auto ».

Les instances de cette classe sont immuables.

## Exemples

Montre comment définir un tableau pour qu'il s'ajuste automatiquement à 50 % de la largeur de la page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

Montre comment définir une largeur préférée pour les cellules du tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Il existe deux manières d'appliquer la classe « PreferredWidth » aux cellules du tableau.
// 1 - Définir une largeur préférée absolue en fonction des points :
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Définir une largeur préférée relative en fonction du pourcentage de la largeur du tableau :
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Une cellule sans largeur préférée spécifiée occupera le reste de l'espace disponible.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Chaque configuration de la propriété « PreferredWidth » crée un nouvel objet.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Voir également

* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
