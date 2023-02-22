---
title: HasSameTemplate
second_title: Aspose.Words for .NET API Reference
description: List method. Returns true if the current list and the given list are created from the same template in C#.
type: docs
weight: 120
url: /net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Returns true if the current list and the given list are created from the same template.

```csharp
public bool HasSameTemplate(List other)
```

## Examples

Shows how to define lists with the same ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### See Also

* class [List](../)
* namespace [Aspose.Words.Lists](../../list/)
* assembly [Aspose.Words](../../../)
