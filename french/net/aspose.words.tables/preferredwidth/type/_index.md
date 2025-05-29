---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PreferredWidth Type, qui définit l'unité de mesure des valeurs de largeur préférées, améliorant ainsi la précision et la flexibilité de votre conception.
type: docs
weight: 40
url: /fr/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

Obtient l'unité de mesure utilisée pour cette valeur de largeur préférée.

```csharp
public PreferredWidthType Type { get; }
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

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
