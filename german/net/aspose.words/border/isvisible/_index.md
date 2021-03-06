---
title: IsVisible
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt true zurück wenn der LineStyle nicht LineStyle.None ist.
type: docs
weight: 30
url: /de/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Gibt „true“ zurück, wenn der LineStyle nicht LineStyle.None ist.

```csharp
public bool IsVisible { get; }
```

### Beispiele

Zeigt, wie Rahmen von einem Absatz entfernt werden.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Jeder Absatz hat einen individuellen Rahmensatz.
// Die Einstellungen für das Aussehen dieser Rahmen erreichen wir über das Objekt Absatzformat.
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

* class [Border](../../border)
* namensraum [Aspose.Words](../../border)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
