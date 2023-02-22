---
title: PreferredWidth.Value
second_title: Référence de l'API Aspose.Words pour .NET
description: PreferredWidth propriété. Obtient la valeur de largeur préférée. Lunité de mesure est précisée dans leType propriété.
type: docs
weight: 50
url: /fr/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Obtient la valeur de largeur préférée. L'unité de mesure est précisée dans le[`Type`](../type/) propriété.

```csharp
public double Value { get; }
```

### Exemples

Montre comment vérifier le type de largeur préféré et la valeur d'une cellule de tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Voir également

* class [PreferredWidth](../)
* espace de noms [Aspose.Words.Tables](../../preferredwidth/)
* Assemblée [Aspose.Words](../../../)


