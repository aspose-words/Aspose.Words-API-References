---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words pour .NET
description: Aspose.Words.Tables.PreferredWidthType énumération. Spécifie lunité de mesure pour la largeur préférée dun tableau ou dune cellule en C#.
type: docs
weight: 6300
url: /fr/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Spécifie l'unité de mesure pour la largeur préférée d'un tableau ou d'une cellule.

```csharp
public enum PreferredWidthType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Auto | `1` | La largeur préférée n'est pas spécifiée. La largeur réelle du tableau ou de la cellule est soit spécifiée à l'aide de la largeur explicite, soit sera déterminée automatiquement par l'algorithme de disposition du tableau lorsque le tableau est affiché, en fonction du paramètre d'ajustement automatique du tableau. |
| Percent | `2` | Mesurez la largeur actuelle de l'élément en utilisant un pourcentage spécifié. |
| Points | `3` | Mesurez la largeur actuelle de l'article en utilisant un nombre spécifié de points (1/72 de pouce). |

## Exemples

Montre comment vérifier le type de largeur préféré et la valeur d’une cellule de tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Voir également

* class [PreferredWidth](../preferredwidth/)
* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
