---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.TextOrientation pour contrôler facilement l'alignement du texte dans les cellules de tableau et les cadres de texte, améliorant ainsi la présentation et la lisibilité du document.
type: docs
weight: 7280
url: /fr/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Spécifie l'orientation du texte sur une page, dans une cellule de tableau ou un cadre de texte.

```csharp
public enum TextOrientation
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Horizontal | `0` | Le texte est disposé horizontalement (lr-tb). |
| Downward | `1` | Le texte est tourné de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl). |
| Upward | `3` | Le texte est tourné de 90 degrés vers la gauche pour apparaître de bas en haut (bt-lr). |
| HorizontalRotatedFarEast | `4` | Le texte est disposé horizontalement, mais les caractères d'Extrême-Orient sont tournés de 90 degrés vers la gauche (gd-db-v). |
| VerticalFarEast | `5` | Les caractères d'Extrême-Orient apparaissent verticalement, les autres textes sont tournés de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Les caractères d'Extrême-Orient apparaissent verticalement, les autres textes sont tournés de 90 degrés vers la droite pour apparaître de haut en bas verticalement, puis de gauche à droite horizontalement (tb-lr-v). |

## Exemples

Montre comment créer un tableau formaté 2x2.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Lors de la construction du tableau, le générateur de documents appliquera ses valeurs de propriété RowFormat/CellFormat actuelles
// à la ligne/cellule actuelle dans laquelle se trouve son curseur et à toutes les nouvelles lignes/cellules au fur et à mesure qu'il les crée.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Les lignes et cellules ajoutées précédemment ne sont pas affectées rétroactivement par les modifications apportées à la mise en forme du générateur.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
