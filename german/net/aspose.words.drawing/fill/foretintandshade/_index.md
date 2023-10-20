---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words für .NET
description: Fill ForeTintAndShade eigendom. Ruft einen DoubleWert ab oder legt diesen fest der die Vordergrundfarbe heller oder dunkler macht in C#.
type: docs
weight: 80
url: /de/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Ruft einen Double-Wert ab oder legt diesen fest, der die Vordergrundfarbe heller oder dunkler macht.

```csharp
public double ForeTintAndShade { get; set; }
```

## Bemerkungen

Die zulässigen Werte liegen für diese Eigenschaft im Bereich von -1 (am dunkelsten) bis 1 (am hellsten). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder mehr als 1 festzulegen, führt zuArgumentOutOfRangeException.

## Beispiele

Zeigt, wie man die Aufhellung und Abdunkelung der Vordergrundschriftfarbe verwaltet.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
