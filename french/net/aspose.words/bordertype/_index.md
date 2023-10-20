---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words pour .NET
description: Aspose.Words.BorderType énumération. Spécifie les côtés dune bordure en C#.
type: docs
weight: 100
url: /fr/net/aspose.words/bordertype/
---
## BorderType enumeration

Spécifie les côtés d'une bordure.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article documentaire.

```csharp
public enum BorderType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `-1` | Valeur par défaut. |
| Bottom | `0` | Spécifie la bordure inférieure d'un paragraphe ou d'une cellule de tableau. |
| Left | `1` | Spécifie la bordure gauche d'un paragraphe ou d'une cellule de tableau. |
| Right | `2` | Spécifie la bordure droite d'un paragraphe ou d'une cellule de tableau. |
| Top | `3` | Spécifie la bordure supérieure d'un paragraphe ou d'une cellule de tableau. |
| Horizontal | `4` | Spécifie la bordure horizontale entre les cellules d'un tableau ou entre les paragraphes conformes. |
| Vertical | `5` | Spécifie la bordure verticale entre les cellules d'un tableau. |
| DiagonalDown | `6` | Spécifie la bordure diagonale dans une cellule de tableau. |
| DiagonalUp | `7` | Spécifie la bordure diagonale dans une cellule de tableau. |

## Exemples

Montre comment insérer un paragraphe avec une bordure supérieure.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Définit ThemeColor uniquement lorsque LineWidth ou LineStyle est défini.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
