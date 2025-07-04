---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Discover the Range Text property to easily retrieve and manipulate text within a specified range for enhanced content management.
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

Assert.That(doc.Range.Text.Trim(), Is.EqualTo("Hello world!"));
```

### See Also

* class [Range](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
