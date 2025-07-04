---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words for .NET
description: Discover if your document includes VBA macros with the FileFormatInfo HasMacros property. Ensure document security and functionality today!
type: docs
weight: 30
url: /net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

Returns `true` if this document contains a VBA macros.

```csharp
public bool HasMacros { get; }
```

## Examples

Shows how to check VBA macro presence without loading document.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.That(fileFormatInfo.HasMacros, Is.True);
```

### See Also

* class [FileFormatInfo](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
