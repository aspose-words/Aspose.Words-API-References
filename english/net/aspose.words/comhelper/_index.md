---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words for .NET
description: Aspose.Words.ComHelper class. Provides methods for COM clients to load a document into Aspose.Words in C#.
type: docs
weight: 390
url: /net/aspose.words/comhelper/
---
## ComHelper class

Provides methods for COM clients to load a document into Aspose.Words.

```csharp
public class ComHelper
```

## Constructors

| Name | Description |
| --- | --- |
| [ComHelper](comhelper/)() | Initializes a new instance of this class. |

## Methods

| Name | Description |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Allows a COM application to load [`Document`](../document/) from a stream. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Allows a COM application to load a [`Document`](../document/) from a file. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Allows a COM application to load a [`Document`](../document/) from an IStream object. |

## Remarks

Use the `ComHelper` class to load a document from a file or stream into a [`Document`](../document/) object in a COM application.

The [`Document`](../document/) class provides a default constructor to create a new document and also provides overloaded constructors to load a document from a file or stream. If you are using Aspose.Words from a .NET application, you can use all of the [`Document`](../document/) constructors directly, but if you are using Aspose.Words from a COM application, only the default [`Document`](../document/) constructor is available.

## Examples

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
