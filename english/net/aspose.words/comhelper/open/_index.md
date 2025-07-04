---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words for .NET
description: Unlock seamless integration with ComHelper's Open method, enabling effortless document loading from files for your COM applications.
type: docs
weight: 20
url: /net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

Allows a COM application to load a [`Document`](../../document/) from a file.

```csharp
public Document Open(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Filename of the document to load. |

### Return Value

A [`Document`](../../document/) object that represents a Word document.

## Remarks

This method is same as calling the [`Document`](../../document/) constructor with a file name parameter.

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

Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello World!\r\rHello Word!\r\r\rHello World!"));

// 2 -  From a stream:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello World!\r\rHello Word!\r\r\rHello World!"));
}
```

### See Also

* class [Document](../../document/)
* class [ComHelper](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

Allows a COM application to load [`Document`](../../document/) from a stream.

```csharp
public Document Open(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | A .NET stream object that contains the document to load. |

### Return Value

A [`Document`](../../document/) object that represents a Word document.

## Remarks

This method is same as calling the [`Document`](../../document/) constructor with a stream parameter.

## Examples

Shows how to open documents using the ComHelper class.

```csharp
// The ComHelper class allows us to load documents from within COM clients.
ComHelper comHelper = new ComHelper();

// 1 -  Using a local system filename:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello World!\r\rHello Word!\r\r\rHello World!"));

// 2 -  From a stream:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello World!\r\rHello Word!\r\r\rHello World!"));
}
```

### See Also

* class [Document](../../document/)
* class [ComHelper](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
