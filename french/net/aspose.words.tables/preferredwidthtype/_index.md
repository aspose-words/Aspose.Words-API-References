---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Tables.PreferredWidthType. Définissez facilement les mesures de largeur des tableaux et des cellules pour une mise en forme précise des documents.
type: docs
weight: 7150
url: /fr/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Spécifie l'unité de mesure de la largeur préférée d'un tableau ou d'une cellule.

```csharp
public enum PreferredWidthType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Auto | `1` | La largeur préférée n'est pas spécifiée. La largeur réelle du tableau ou de la cellule est soit spécifiée explicitement, soit déterminée automatiquement par l'algorithme de mise en page du tableau lors de son affichage, selon le paramètre d'ajustement automatique du tableau. |
| Percent | `2` | Mesurez la largeur de l'élément actuel à l'aide d'un pourcentage spécifié. |
| Points | `3` | Mesurez la largeur de l'élément actuel à l'aide d'un nombre de points spécifié (1/72 pouce). |

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

* class [PreferredWidth](../preferredwidth/)
* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
