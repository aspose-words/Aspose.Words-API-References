---
title: ControlChar.TabChar
second_title: Aspose.Words för .NET API Referens
description: ControlChar fält. Tabtecken char9 eller t.
type: docs
weight: 280
url: /sv/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Tab-tecken: (char)9 eller "\t".

```csharp
public const char TabChar;
```

### Exempel

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
* namnutrymme [Aspose.Words](../../controlchar/)
* hopsättning [Aspose.Words](../../../)


