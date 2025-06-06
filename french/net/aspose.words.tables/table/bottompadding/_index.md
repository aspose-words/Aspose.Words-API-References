---
title: Table.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Table BottomPadding, ajustez facilement l'espacement sous le contenu des cellules pour un contrôle de mise en page amélioré et un attrait visuel amélioré.
type: docs
weight: 90
url: /fr/net/aspose.words.tables/table/bottompadding/
---
## Table.BottomPadding property

Obtient ou définit la quantité d'espace (en points) à ajouter sous le contenu des cellules.

```csharp
public double BottomPadding { get; set; }
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
