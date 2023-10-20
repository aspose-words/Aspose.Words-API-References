---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words för .NET
description: Font Italic fast egendom. Sant om teckensnittet är formaterat som kursivt i C#.
type: docs
weight: 160
url: /sv/net/aspose.words/font/italic/
---
## Font.Italic property

Sant om teckensnittet är formaterat som kursivt.

```csharp
public bool Italic { get; set; }
```

## Exempel

Visar hur man skriver kursiv text med hjälp av en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
