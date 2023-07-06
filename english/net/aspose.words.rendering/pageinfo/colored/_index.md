---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words for .NET
description: PageInfo Colored property. Returns true if the page contains colored content in C#.
type: docs
weight: 10
url: /net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Returns `true` if the page contains colored content.

```csharp
public bool Colored { get; }
```

## Examples

Shows how to check whether the page is in color or not.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Check that the first page of the document is not colored.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### See Also

* class [PageInfo](../)
* namespace [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assembly [Aspose.Words](../../../)
