---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words for .NET
description: Document DefaultTabStop property. Gets or sets the interval in points between the default tab stops in C#.
type: docs
weight: 90
url: /net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Gets or sets the interval (in points) between the default tab stops.

```csharp
public double DefaultTabStop { get; set; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)
