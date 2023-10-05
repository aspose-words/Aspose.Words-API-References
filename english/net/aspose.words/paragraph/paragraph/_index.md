---
title: Paragraph
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words for .NET
description: Paragraph constructor. Initializes a new instance of the Paragraph class in C#.
type: docs
weight: 10
url: /net/aspose.words/paragraph/paragraph/
---
## Paragraph constructor

Initializes a new instance of the [`Paragraph`](../) class.

```csharp
public Paragraph(DocumentBase doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |

## Remarks

When [`Paragraph`](../) is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../node/parentnode/) is `null`.

To append [`Paragraph`](../) to the document use [`InsertAfter`](../../compositenode/insertafter/) or [`InsertBefore`](../../compositenode/insertbefore/) on the story where you want the paragraph inserted.

### See Also

* class [DocumentBase](../../documentbase/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
