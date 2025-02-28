---
title: ParagraphCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words for .NET
description: Effortlessly convert your ParagraphCollection to an array with the ToArray method, streamlining data management and enhancing your document processing.
type: docs
weight: 20
url: /net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

Copies all paragraphs from the collection to a new array of paragraphs.

```csharp
public Paragraph[] ToArray()
```

### Return Value

An array of paragraphs.

## Examples

Shows how to create an array from a NodeCollection.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

Shows how to use "hot remove" to remove a node during enumeration.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// Remove a node from the collection in the middle of an enumeration.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### See Also

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
