---
title: Table.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words pour .NET
description: Ajustez la propriété DistanceBottom du tableau pour contrôler l'espacement entre le bas de votre tableau et le texte environnant, améliorant ainsi la mise en page et la lisibilité.
type: docs
weight: 120
url: /fr/net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

Obtient ou définit la distance entre le bas du tableau et le texte environnant, en points.

```csharp
public double DistanceBottom { get; set; }
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

// Définir la distance entre le tableau et le texte environnant.
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
