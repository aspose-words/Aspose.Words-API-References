---
title: ComHelper
second_title: Aspose.Words for .NET API Reference
description: ComHelper constructor. Initializes a new instance of this class in C#.
type: docs
weight: 10
url: /net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Initializes a new instance of this class.

```csharp
public ComHelper()
```

## Examples

Shows how to open documents using the ComHelper class.

```csharp
// The ComHelper class allows us to load documents from within COM clients.
ComHelper comHelper = new ComHelper();

// 1 -  Using a local system filename:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 -  From a stream:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### See Also

* class [ComHelper](../)
* namespace [Aspose.Words](../../comhelper/)
* assembly [Aspose.Words](../../../)
