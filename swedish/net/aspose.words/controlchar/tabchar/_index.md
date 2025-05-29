---
title: ControlChar.TabChar
linktitle: TabChar
articleTitle: TabChar
second_title: Aspose.Words för .NET
description: Bemästra TabChar-fält med ControlChar för sömlös datahantering. Lås upp effektiviteten med det mångsidiga tabbtecknet (char9 eller t) idag!
type: docs
weight: 280
url: /sv/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Tab-tecken: (char)9 eller "\t".

```csharp
public const char TabChar;
```

## Exempel

Visar hur man ställer in ett anpassat intervall för tabbstoppspositioner.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in tabbstopp så att de visas var 72:e punkt (1 tum).
builder.Document.DefaultTabStop = 72;

// Varje tabbtecken fäster texten efter det till nästa närmaste tabbstoppsposition.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Se även

* class [ControlChar](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
