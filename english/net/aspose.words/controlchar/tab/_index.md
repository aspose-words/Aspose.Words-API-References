---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words for .NET
description: Discover the ControlChar Tab field, understand the Tab character x0009 for efficient text formatting and enhanced data management.
type: docs
weight: 270
url: /net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Tab character: "\x0009" or "\t".

```csharp
public static readonly string Tab;
```

## Examples

Shows how to set a custom interval for tab stop positions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set tab stops to appear every 72 points (1 inch).
builder.Document.DefaultTabStop = 72;

// Each tab character snaps the text after it to the next closest tab stop position.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### See Also

* class [ControlChar](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
