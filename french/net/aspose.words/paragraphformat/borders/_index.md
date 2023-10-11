---
title: ParagraphFormat.Borders
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Récupère la collection de bordures du paragraphe.
type: docs
weight: 60
url: /fr/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Récupère la collection de bordures du paragraphe.

```csharp
public BorderCollection Borders { get; }
```

### Exemples

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

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


