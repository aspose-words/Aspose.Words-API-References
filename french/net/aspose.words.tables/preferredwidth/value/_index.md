---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words pour .NET
description: Découvrez la propriété « Valeur de largeur préférée » pour accéder facilement à votre largeur préférée et la personnaliser. Améliorez votre design avec des mesures précises dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Récupère la valeur de largeur préférée. L'unité de mesure est spécifiée dans le[`Type`](../type/) propriété.

```csharp
public double Value { get; }
```

## Exemples

Montre comment vérifier le type de largeur et la valeur préférés d'une cellule de tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Voir également

* class [PreferredWidth](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
