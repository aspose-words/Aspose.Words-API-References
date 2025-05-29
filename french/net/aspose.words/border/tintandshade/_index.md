---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words pour .NET
description: Découvrez Border TintAndShade, ajustez facilement la luminosité des couleurs grâce à une simple double valeur pour des designs époustouflants. Idéal pour vos projets créatifs !
type: docs
weight: 80
url: /fr/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur.

```csharp
public double TintAndShade { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lève une exception si vous tentez de définir cette propriété sur une valeur inférieure à -1 ou supérieure à 1. |
| InvalidOperationException | Lève si cette propriété est définie pour un objet Border avec des couleurs non thématiques. |

## Remarques

Les valeurs autorisées sont comprises entre -1 (le plus foncé) et 1 (le plus clair) pour cette propriété. Zéro (0) est neutre.

## Exemples

Montre comment insérer un paragraphe avec une bordure supérieure.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Définissez ThemeColor uniquement lorsque LineWidth ou LineStyle est défini.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Voir également

* class [Border](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
