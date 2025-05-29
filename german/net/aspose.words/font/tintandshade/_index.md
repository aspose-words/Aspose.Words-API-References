---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font TintAndShade-Eigenschaft, um Farben einfach anzupassen! Hellen oder verdunkeln Sie Farbtöne für lebendige Designs. Optimieren Sie Ihre Projekte mühelos!
type: docs
weight: 530
url: /de/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der eine Farbe aufhellt oder abdunkelt.

```csharp
public double TintAndShade { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 gesetzt wird. |
| InvalidOperationException | Auslösen, wenn diese Eigenschaft für festgelegt ist[`Font`](../) Objekt mit nicht zum Thema gehörenden Farben. |

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (am dunkelsten) bis 1 (am hellsten).

Null (0) ist neutral.

## Beispiele

Zeigt, wie man einen Themenstil erstellt und verwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Erstellen Sie einen Stil mit den Schrifteigenschaften des Designs.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
