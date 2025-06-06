---
title: DocumentBuilder.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words pour .NET
description: Explorez la propriété ParagraphFormat de DocumentBuilder pour accéder et personnaliser les fonctionnalités essentielles de formatage de paragraphe pour un style de document amélioré.
type: docs
weight: 170
url: /fr/net/aspose.words/documentbuilder/paragraphformat/
---
## DocumentBuilder.ParagraphFormat property

Renvoie un objet qui représente les propriétés de formatage de paragraphe actuelles.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## Exemples

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

* class [ParagraphFormat](../../paragraphformat/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
