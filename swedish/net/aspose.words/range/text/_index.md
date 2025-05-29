---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Textintervall för att enkelt hämta och manipulera text inom ett angivet intervall för förbättrad innehållshantering.
type: docs
weight: 60
url: /sv/net/aspose.words/range/text/
---
## Range.Text property

Hämtar texten i intervallet.

```csharp
public string Text { get; }
```

## Anmärkningar

Den returnerade strängen innehåller alla kontroll- och specialtecken enligt beskrivningen i[`ControlChar`](../../controlchar/).

## Exempel

Visar hur man hämtar textinnehållet för alla noder som ett område täcker.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Se även

* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
