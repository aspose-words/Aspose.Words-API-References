---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words pour .NET
description: Border TintAndShade propriété. Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur en C#.
type: docs
weight: 80
url: /fr/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur.

```csharp
public double TintAndShade { get; set; }
```

## Remarques

Les valeurs autorisées sont comprises entre -1 (le plus sombre) et 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété sur une valeur inférieure à -1 ou supérieure à 1 entraîneArgumentOutOfRangeException.

La définition de cette propriété pour l'objet Border avec des couleurs non thématiques entraîneInvalidOperationException.

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

* class [Border](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
