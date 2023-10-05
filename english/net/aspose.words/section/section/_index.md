---
title: Section
linktitle: Section
articleTitle: Section
second_title: Aspose.Words for .NET
description: Section constructor. Initializes a new instance of the Section class in C#.
type: docs
weight: 10
url: /net/aspose.words/section/section/
---
## Section constructor

Initializes a new instance of the Section class.

```csharp
public Section(DocumentBase doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |

## Remarks

When the section is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../node/parentnode/) is `null`.

To include [`Section`](../) into a document use [`InsertAfter`](../../compositenode/insertafter/) and [`InsertBefore`](../../compositenode/insertbefore/) methods of the [`Document`](../../document/) OR [`Add`](../../nodecollection/add/) and [`Insert`](../../nodecollection/insert/) methods of the [`Sections`](../../document/sections/) property.

### See Also

* class [DocumentBase](../../documentbase/)
* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
