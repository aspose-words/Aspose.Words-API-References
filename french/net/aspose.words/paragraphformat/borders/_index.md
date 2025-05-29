---
title: ParagraphFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat Borders pour gérer et personnaliser facilement vos bordures de paragraphe, améliorant ainsi l'esthétique et la lisibilité du document.
type: docs
weight: 60
url: /fr/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Obtient la collection des bordures du paragraphe.

```csharp
public BorderCollection Borders { get; }
```

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

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
