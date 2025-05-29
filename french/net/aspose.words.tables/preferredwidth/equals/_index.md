---
title: PreferredWidth.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode PreferredWidth Equals vérifie si la largeur spécifiée correspond à la valeur actuelle, garantissant ainsi la précision de la conception de votre mise en page.
type: docs
weight: 60
url: /fr/net/aspose.words.tables/preferredwidth/equals/
---
## Equals(*[PreferredWidth](../)*) {#equals}

Détermine si le spécifié[`PreferredWidth`](../) est égal en valeur au courant[`PreferredWidth`](../) .

```csharp
public bool Equals(PreferredWidth other)
```

## Exemples

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

* class [PreferredWidth](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

Détermine si l'objet spécifié est égal en valeur à l'objet actuel.

```csharp
public override bool Equals(object obj)
```

## Exemples

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

* class [PreferredWidth](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
