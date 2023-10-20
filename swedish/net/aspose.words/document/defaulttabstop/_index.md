---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words för .NET
description: Document DefaultTabStop fast egendom. Hämtar eller ställer in intervallet i poäng mellan standardtabbstoppen i C#.
type: docs
weight: 90
url: /sv/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Hämtar eller ställer in intervallet (i poäng) mellan standardtabbstoppen.

```csharp
public double DefaultTabStop { get; set; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
