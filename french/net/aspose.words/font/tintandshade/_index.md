---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font TintAndShade pour ajuster facilement les couleurs ! Éclaircissez ou assombrissez les nuances pour des designs éclatants. Sublimez vos projets sans effort !
type: docs
weight: 530
url: /fr/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur.

```csharp
public double TintAndShade { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lancer si cette propriété est définie sur une valeur inférieure à -1 ou supérieure à 1. |
| InvalidOperationException | Lancer si cette propriété est définie pour[`Font`](../) objet avec des couleurs non thématiques. |

## Remarques

Les valeurs autorisées sont comprises entre -1 (le plus sombre) et 1 (le plus clair) pour cette propriété.

Zéro (0) est neutre.

## Exemples

Montre comment créer et utiliser un style thématique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Créez du style avec les propriétés de police du thème.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
