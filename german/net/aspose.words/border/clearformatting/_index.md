---
title: Border.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words für .NET
description: Setzen Sie Ihre Rahmeneigenschaften mit der Methode „Border ClearFormatting“ auf die Standardeinstellungen zurück. Vereinfachen Sie Ihren Designprozess und verbessern Sie die Darstellung Ihres Projekts!
type: docs
weight: 90
url: /de/net/aspose.words/border/clearformatting/
---
## Border.ClearFormatting method

Setzt die Rahmeneigenschaften auf die Standardwerte zurück.

```csharp
public void ClearFormatting()
```

## Bemerkungen

Wenn die Rahmeneigenschaften auf die Standardwerte zurückgesetzt werden, ist der Rahmen unsichtbar.

## Beispiele

Zeigt, wie man Rahmen aus einem Absatz entfernt.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Jeder Absatz hat einen individuellen Satz von Rahmen.
// Auf die Einstellungen für die Darstellung dieser Rahmen können wir über das Absatzformatobjekt zugreifen.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

    // Wir können einen Rahmen sofort entfernen, indem wir die Methode ClearFormatting ausführen.
// Wenn Sie diese Methode auf jeden Rand eines Absatzes anwenden, werden alle seine Ränder entfernt.
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
