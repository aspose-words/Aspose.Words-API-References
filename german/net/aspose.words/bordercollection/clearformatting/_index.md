---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ClearFormatting-Methode „BorderCollection“ mühelos alle Objektränder entfernt und Ihr Design mit klaren, scharfen Bildern aufwertet.
type: docs
weight: 140
url: /de/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Entfernt alle Ränder eines Objekts.

```csharp
public void ClearFormatting()
```

## Beispiele

Zeigt, wie Sie alle Rahmen aus allen Absätzen in einem Dokument entfernen.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Der erste Absatz dieses Dokuments hat mit diesen Einstellungen sichtbare Ränder.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Verwenden Sie die Methode „ClearFormatting“ für jeden Absatz, um alle Rahmen zu entfernen.
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
        Assert.AreEqual(LineStyle.None, border.LineStyle);
        Assert.AreEqual(0.0d, border.LineWidth);
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### Siehe auch

* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
