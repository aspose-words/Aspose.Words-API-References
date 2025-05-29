---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Kursiv stil! Formatera enkelt text i kursiv stil för att förbättra läsbarheten och stilen i dina designer. Förbättra din typografi idag!
type: docs
weight: 160
url: /sv/net/aspose.words/font/italic/
---
## Font.Italic property

Sant om teckensnittet är formaterat som kursiv stil.

```csharp
public bool Italic { get; set; }
```

## Exempel

Visar hur man skriver kursiverad text med hjälp av en dokumentbyggare.

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
