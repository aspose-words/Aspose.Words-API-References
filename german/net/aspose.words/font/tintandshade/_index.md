---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words für .NET
description: Font TintAndShade eigendom. Ruft einen DoubleWert ab oder legt ihn fest der eine Farbe heller oder dunkler macht in C#.
type: docs
weight: 520
url: /de/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der eine Farbe heller oder dunkler macht.

```csharp
public double TintAndShade { get; set; }
```

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (am dunkelsten) bis 1 (am hellsten). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder mehr als 1 festzulegen, führt zu einemArgumentOutOfRangeException.

Festlegen dieser Eigenschaft für[`Font`](../) Objekt mit Nicht-Theme-Farben führt zu aInvalidOperationException.

## Beispiele

Zeigt, wie ein Themenstil erstellt und verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Erstellen Sie einen Stil mit den Schriftarteigenschaften des Themas.
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
