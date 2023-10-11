---
title: BorderCollection.ClearFormatting
second_title: Aspose.Words für .NET-API-Referenz
description: BorderCollection methode. Entfernt alle Ränder eines Objekts.
type: docs
weight: 140
url: /de/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Entfernt alle Ränder eines Objekts.

```csharp
public void ClearFormatting()
```

### Beispiele

Zeigt, wie alle Ränder aus allen Absätzen in einem Dokument entfernt werden.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Der erste Absatz dieses Dokuments hat sichtbare Ränder mit diesen Einstellungen.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Verwenden Sie die Methode „ClearFormatting“ für jeden Absatz, um alle Ränder zu entfernen.
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
* namensraum [Aspose.Words](../../bordercollection/)
* Montage [Aspose.Words](../../../)


