---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words per .NET
description: Scopri come il metodo BorderCollection ClearFormatting rimuove senza sforzo tutti i bordi degli oggetti, migliorando il tuo design con immagini pulite e nitide.
type: docs
weight: 140
url: /it/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Rimuove tutti i bordi di un oggetto.

```csharp
public void ClearFormatting()
```

## Esempi

Mostra come rimuovere tutti i bordi da tutti i paragrafi di un documento.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Con queste impostazioni, il primo paragrafo di questo documento presenta bordi visibili.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Utilizzare il metodo "ClearFormatting" su ogni paragrafo per rimuovere tutti i bordi.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
