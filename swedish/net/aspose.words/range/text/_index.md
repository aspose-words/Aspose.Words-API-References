---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Range Text fast egendom. Hämtar intervallets text i C#.
type: docs
weight: 60
url: /sv/net/aspose.words/range/text/
---
## Range.Text property

Hämtar intervallets text.

```csharp
public string Text { get; }
```

## Anmärkningar

Den returnerade strängen innehåller alla kontroll- och specialtecken som beskrivs i[`ControlChar`](../../controlchar/).

## Exempel

Visar hur man får fram textinnehållet för alla noder som ett intervall täcker.

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
