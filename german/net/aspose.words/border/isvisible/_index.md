---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words für .NET
description: Border IsVisible eigendom. Gibt zurückWAHR wenn dieLineStyle ist nichtNone  in C#.
type: docs
weight: 30
url: /de/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Gibt zurück`WAHR` wenn die[`LineStyle`](../linestyle/) ist nichtNone .

```csharp
public bool IsVisible { get; }
```

## Beispiele

Zeigt, wie Rahmen aus einem Absatz entfernt werden.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Jeder Absatz hat einen individuellen Satz von Rahmen.
// Auf die Einstellungen für das Aussehen dieser Ränder können wir über das Absatzformatobjekt zugreifen.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // Wir können einen Rahmen sofort entfernen, indem wir die ClearFormatting-Methode ausführen.
// Wenn Sie diese Methode an jedem Rand eines Absatzes ausführen, werden alle seine Ränder entfernt.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### Siehe auch

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
