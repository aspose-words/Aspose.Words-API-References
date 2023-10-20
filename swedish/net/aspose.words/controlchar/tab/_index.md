---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words för .NET
description: ControlChar Tab fält. Tabtecken x0009 eller t i C#.
type: docs
weight: 270
url: /sv/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Tab-tecken: "\x0009" eller "\t".

```csharp
public static readonly string Tab;
```

## Exempel

Visar hur man ställer in ett anpassat intervall för tabbstopppositioner.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in tabbstopp för att visas var 72:e punkt (1 tum).
builder.Document.DefaultTabStop = 72;

// Varje tabbtecken fäster texten efter den till nästa tabbstoppposition.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Se även

* class [ControlChar](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
