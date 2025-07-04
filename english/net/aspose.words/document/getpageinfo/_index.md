---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words for .NET
description: Discover the GetPageInfo method to retrieve essential page size, orientation, and rendering details for optimized printing and enhanced document management.
type: docs
weight: 650
url: /net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

Gets the page size, orientation and other information about a page that might be useful for printing or rendering.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | Int32 | The 0-based page index. |

## Examples

Shows how to check whether the page is in color or not.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Check that the first page of the document is not colored.
Assert.That(doc.GetPageInfo(0).Colored, Is.False);
```

### See Also

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
