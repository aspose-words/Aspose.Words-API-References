---
title: Enum BorderType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.BorderType énumération. Spécifie les côtés dune bordure.
type: docs
weight: 90
url: /fr/net/aspose.words/bordertype/
---
## BorderType enumeration

Spécifie les côtés d'une bordure.

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

### Exemples

Montre comment insérer un paragraphe avec une bordure supérieure.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


