---
title: BorderCollection.ClearFormatting
second_title: Aspose.Words per .NET API Reference
description: BorderCollection metodo. Rimuove tutti i bordi di un oggetto.
type: docs
weight: 140
url: /it/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Rimuove tutti i bordi di un oggetto.

```csharp
public void ClearFormatting()
```

### Esempi

Mostra come rimuovere tutti i bordi da tutti i paragrafi in un documento.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Il primo paragrafo di questo documento ha bordi visibili con queste impostazioni.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Usa il metodo "ClearFormatting" su ogni paragrafo per rimuovere tutti i bordi.
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

### Guarda anche

* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../bordercollection/)
* assemblea [Aspose.Words](../../../)


