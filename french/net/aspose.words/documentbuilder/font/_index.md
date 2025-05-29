---
title: DocumentBuilder.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words pour .NET
description: Explorez la propriété Police de DocumentBuilder pour accéder à votre mise en forme de police actuelle et la personnaliser facilement. Améliorez le style de votre document dès aujourd'hui !
type: docs
weight: 100
url: /fr/net/aspose.words/documentbuilder/font/
---
## DocumentBuilder.Font property

Renvoie un objet qui représente les propriétés de formatage de police actuelles.

```csharp
public Font Font { get; }
```

## Remarques

Utiliser`Font` pour accéder et modifier les propriétés de formatage des polices.

Spécifiez le formatage de la police avant d'insérer du texte.

## Exemples

Montre comment insérer une chaîne entourée d'une bordure dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Montre comment créer un tableau formaté à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Définissez certaines options de formatage pour l'apparence du texte et du tableau.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// La configuration des options de formatage dans un générateur de documents les appliquera
// à la cellule/ligne actuelle dans laquelle se trouve son curseur,
// ainsi que toutes les nouvelles cellules et lignes créées à l'aide de ce générateur.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Reconfigurez les objets de formatage du générateur pour les nouvelles lignes et cellules que nous sommes sur le point de créer.
// Le constructeur ne les appliquera pas à la première ligne déjà créée afin qu'elle se démarque comme une ligne d'en-tête.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Voir également

* class [Font](../../font/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
