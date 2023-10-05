---
title: Node.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: Node GetText method. Gets the text of this node and of all its children in C#.
type: docs
weight: 120
url: /net/aspose.words/node/gettext/
---
## Node.GetText method

Gets the text of this node and of all its children.

```csharp
public virtual string GetText()
```

## Remarks

The returned string includes all control and special characters as described in [`ControlChar`](../../controlchar/).

## Examples

Shows how to use control characters.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert paragraphs with text with DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Converting the document to text form reveals that control characters
// represent some of the document's structural elements, such as page breaks.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// When converting a document to string form,
// we can omit some of the control characters with the Trim method.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### See Also

* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
