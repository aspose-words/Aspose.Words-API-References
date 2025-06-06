---
title: ParagraphCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words för .NET
description: Konvertera enkelt din ParagraphCollection till en array med ToArray-metoden, vilket effektiviserar datahanteringen och förbättrar din dokumentbehandling.
type: docs
weight: 20
url: /sv/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

Kopierar alla stycken från samlingen till en ny matris med stycken.

```csharp
public Paragraph[] ToArray()
```

### Returvärde

En matris med stycken.

## Exempel

Visar hur man skapar en array från en NodeCollection.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

Visar hur man använder "hot remove" för att ta bort en nod under uppräkning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// Ta bort en nod från samlingen mitt i en uppräkning.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### Se även

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
