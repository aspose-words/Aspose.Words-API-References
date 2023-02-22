---
title: Document.DefaultTabStop
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Hämtar eller ställer in intervallet i poäng mellan standardtabbstoppen.
type: docs
weight: 90
url: /sv/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Hämtar eller ställer in intervallet (i poäng) mellan standardtabbstoppen.

```csharp
public double DefaultTabStop { get; set; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


