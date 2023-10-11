---
title: Border.ThemeColor
second_title: Référence de l'API Aspose.Words pour .NET
description: Border propriété. Obtient ou définit la couleur du thème dans le jeu de couleurs appliqué associé à cet objet Border.
type: docs
weight: 70
url: /fr/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Obtient ou définit la couleur du thème dans le jeu de couleurs appliqué associé à cet objet Border.

```csharp
public ThemeColor ThemeColor { get; set; }
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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* espace de noms [Aspose.Words](../../border/)
* Assemblée [Aspose.Words](../../../)


