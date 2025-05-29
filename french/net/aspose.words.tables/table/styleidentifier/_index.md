---
title: Table.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Table StyleIdentifier pour gérer facilement les styles de tableau indépendants des paramètres régionaux, améliorant ainsi la présentation de vos données sans effort.
type: docs
weight: 280
url: /fr/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

Obtient ou définit l'identifiant de style indépendant des paramètres régionaux du style de table appliqué à cette table.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Exemples

Montre comment créer un nouveau tableau tout en appliquant un style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Nous devons insérer au moins une ligne avant de définir un formatage de tableau.
builder.InsertCell();

// Définissez le style de tableau utilisé en fonction de l'identifiant de style.
// Notez que tous les styles de tableau ne sont pas disponibles lors de l'enregistrement au format .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Appliquez partiellement le style aux fonctionnalités de la table en fonction des prédicats, puis créez la table.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Voir également

* enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
