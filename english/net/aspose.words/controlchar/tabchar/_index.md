---
title: ControlChar.TabChar
linktitle: TabChar
second_title: Aspose.Words for .NET API Reference
description: ControlChar TabChar field. Tab character char9 or t in C#.
type: docs
weight: 280
url: /net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Tab character: (char)9 or "\t".

```csharp
public const char TabChar;
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
* namespace [Aspose.Words](../../controlchar/)
* assembly [Aspose.Words](../../../)
