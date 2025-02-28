---
title: VbaProject.IsProtected
linktitle: IsProtected
articleTitle: IsProtected
second_title: Aspose.Words for .NET
description: Discover if your VbaProject is password protected with the IsProtected property. Ensure your code's security and streamline project management effectively!
type: docs
weight: 30
url: /net/aspose.words.vba/vbaproject/isprotected/
---
## VbaProject.IsProtected property

Shows whether the [`VbaProject`](../) is password protected.

```csharp
public bool IsProtected { get; }
```

## Examples

Shows whether the VbaProject is password protected.

```csharp
Document doc = new Document(MyDir + "Vba protected.docm");
Assert.True(doc.VbaProject.IsProtected);
```

### See Also

* class [VbaProject](../)
* namespace [Aspose.Words.Vba](../../../aspose.words.vba/)
* assembly [Aspose.Words](../../../)
