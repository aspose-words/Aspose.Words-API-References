---
title: Class PreferredWidth
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Tables.PreferredWidth classe. Représente une valeur et son unité de mesure utilisée pour spécifier la largeur préférée dun tableau ou dune cellule.
type: docs
weight: 6290
url: /fr/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Représente une valeur et son unité de mesure utilisée pour spécifier la largeur préférée d'un tableau ou d'une cellule.

Pour en savoir plus, visitez le[Travailler avec des tableaux](https://docs.aspose.com/words/net/working-with-tables/) article documentaire.

```csharp
public sealed class PreferredWidth
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Obtient l'unité de mesure utilisée pour cette valeur de largeur préférée. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Obtient la valeur de largeur préférée. L'unité de mesure est spécifiée dans le[`Type`](./type/) propriété. |

## Méthodes

| Nom | La description |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(double) | Une méthode de création qui renvoie une nouvelle instance qui représente une largeur préférée spécifiée sous forme de pourcentage. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(double) | Une méthode de création qui renvoie une nouvelle instance qui représente une largeur préférée spécifiée à l'aide d'un nombre de points. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(object) | Détermine si l'objet spécifié a une valeur égale à l'objet actuel. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(PreferredWidth) | Détermine si le`PreferredWidth` est égale en valeur au courant`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Sert de fonction de hachage pour ce type. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |

## Des champs

| Nom | La description |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | Renvoie une instance qui représente la valeur « la largeur préférée n'est pas spécifiée ». |

### Remarques

La largeur préférée peut être spécifiée sous forme de pourcentage, de nombre de points ou d'une valeur spéciale « aucun/auto ».

Les instances de cette classe sont immuables.

### Exemples

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

// Il existe deux manières d'appliquer la classe "PreferredWidth" aux cellules d'un tableau.
// 1 - Définit une largeur préférée absolue basée sur les points :
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Définit une largeur préférée relative basée sur le pourcentage de la largeur du tableau :
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Une cellule sans largeur préférée spécifiée occupera le reste de l'espace disponible.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Chaque configuration de la propriété "PreferredWidth" crée un nouvel objet.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Voir également

* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)


