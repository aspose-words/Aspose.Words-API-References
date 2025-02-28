---
title: ControlChar.TabChar
linktitle: TabChar
articleTitle: TabChar
second_title: Aspose.Words for .NET
description: Master TabChar fields with ControlChar for seamless data management. Unlock efficiency with the versatile tab character (char9 or t) today!
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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
