---
title: Range.Text
linktitle: Text
second_title: Aspose.Words for .NET API Reference
description: Range property. Gets the text of the range in C#.
type: docs
weight: 60
url: /net/aspose.words/range/text/
---
## Range.Text property

Gets the text of the range.

```csharp
public string Text { get; }
```

## Remarks

The returned string includes all control and special characters as described in [`ControlChar`](../../controlchar/).

## Examples

Shows how to get the text contents of all the nodes that a range covers.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### See Also

* class [Range](../)
* namespace [Aspose.Words](../../range/)
* assembly [Aspose.Words](../../../)
