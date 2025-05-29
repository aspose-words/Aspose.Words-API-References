---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar egenskapen DefaultTabStop för att ange exakta tabbintervall i punkter, vilket förbättrar formatering och layout i ditt dokument.
type: docs
weight: 100
url: /sv/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Hämtar eller ställer in intervallet (i punkter) mellan standardtabbstoppen.

```csharp
public double DefaultTabStop { get; set; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
