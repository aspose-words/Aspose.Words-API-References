---
title: Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words for .NET
description: Body constructor. Initializes a new instance of the Body class in C#.
type: docs
weight: 10
url: /net/aspose.words/body/body/
---
## Body constructor

Initializes a new instance of the [`Body`](../) class.

```csharp
public Body(DocumentBase doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |

## Remarks

When [`Body`](../) is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../node/parentnode/) is `null`.

To append [`Body`](../) to a [`Section`](../../section/) use [`AppendChild`](../../compositenode/appendchild/), [`InsertAfter`](../../compositenode/insertafter/) or [`InsertBefore`](../../compositenode/insertbefore/) methods.

### See Also

* class [DocumentBase](../../documentbase/)
* class [Body](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
