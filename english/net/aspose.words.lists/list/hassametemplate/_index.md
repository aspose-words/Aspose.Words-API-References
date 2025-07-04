---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words for .NET
description: Discover the HasSameTemplate method, easily check if two lists share the same template, ensuring consistency and efficiency in your data management.
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

Assert.That(doc.Lists[0].HasSameTemplate(doc.Lists[1]), Is.True);
Assert.That(doc.Lists[1].HasSameTemplate(doc.Lists[2]), Is.False);
```

### See Also

* class [List](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
