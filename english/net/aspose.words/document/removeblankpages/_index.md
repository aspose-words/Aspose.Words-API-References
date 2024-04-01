---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words for .NET
description: Document RemoveBlankPages method. Removes blank pages from the document in C#.
type: docs
weight: 690
url: /net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

Removes blank pages from the document.

```csharp
public List<int> RemoveBlankPages()
```

### Return Value

List of page numbers has been considered as blank and removed.

## Remarks

The resulting document will not contain pages considered to be blank while other content, including numbering, headers/footers and overall layout should remain unchanged. Page is considered to be blank when body of the page have no visible content, for example, empty table having no borders will be considered as invisible and therefore page will be detected as blank.

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
