---
title: Table.DistanceTop
linktitle: DistanceTop
articleTitle: DistanceTop
second_title: Aspose.Words pour .NET
description: Ajustez facilement la distance entre le plateau de votre table et le texte environnant. Améliorez votre mise en page pour un rendu soigné et professionnel avec DistanceTop !
type: docs
weight: 150
url: /fr/net/aspose.words.tables/table/distancetop/
---
## Table.DistanceTop property

Obtient ou définit la distance entre le dessus de la table et le texte environnant, en points.

```csharp
public double DistanceTop { get; set; }
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
