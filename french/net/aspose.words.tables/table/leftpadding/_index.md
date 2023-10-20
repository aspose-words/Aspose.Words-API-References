---
title: Table.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words pour .NET
description: Table LeftPadding propriété. Obtient ou définit la quantité despace en points à ajouter à gauche du contenu des cellules en C#.
type: docs
weight: 200
url: /fr/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

Obtient ou définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules.

```csharp
public double LeftPadding { get; set; }
```

## Exemples

Montre comment configurer le remplissage du contenu dans un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Pour chaque cellule du tableau, définissez la distance entre son contenu et chacune de ses bordures.
// Ce tableau conservera la distance de remplissage minimale en enveloppant le texte.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
