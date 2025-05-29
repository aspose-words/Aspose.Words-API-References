---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words für .NET
description: Passen Sie die Eigenschaft „ForeTintAndShade“ an, um Ihre Vordergrundfarbe einfach aufzuhellen oder abzudunkeln und so Ihr Design mit Präzision und Kreativität zu verbessern.
type: docs
weight: 90
url: /de/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der die Vordergrundfarbe aufhellt oder abdunkelt.

```csharp
public double ForeTintAndShade { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 gesetzt wird. |

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (dunkelster Wert) bis 1 (hellster Wert).

Null (0) ist neutral.

## Beispiele

Zeigt, wie Sie die Vordergrundschriftfarbe aufhellen und abdunkeln.

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
