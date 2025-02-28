---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words for .NET
description: Effortlessly clear sections with the ClearContent method. Enhance your workflow and improve content management efficiency today!
type: docs
weight: 110
url: /net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Clears the section.

```csharp
public void ClearContent()
```

## Remarks

The text of [`Body`](../body/) is cleared, only one empty paragraph is left that represents the section break.

The text of all headers and footers is cleared, but [`HeaderFooter`](../../headerfooter/) objects themselves are not removed.

## Examples

Shows how to clear the contents of a section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Running the "ClearContent" method will remove all the section contents
// but leave a blank paragraph to add content again.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
