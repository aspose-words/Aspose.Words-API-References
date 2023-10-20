---
title: Table.DistanceLeft
linktitle: DistanceLeft
articleTitle: DistanceLeft
second_title: Aspose.Words pour .NET
description: Table DistanceLeft propriété. Obtient ou définit la distance entre la gauche du tableau et le texte environnant en points en C#.
type: docs
weight: 130
url: /fr/net/aspose.words.tables/table/distanceleft/
---
## Table.DistanceLeft property

Obtient ou définit la distance entre la gauche du tableau et le texte environnant, en points.

```csharp
public double DistanceLeft { get; set; }
```

## Exemples

Montre comment définir la distance entre les limites du tableau et le texte.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

 // Définit la distance entre le tableau et le texte environnant.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
