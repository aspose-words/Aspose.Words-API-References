---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words för .NET
description: Upptäck Font NoProofing. Förhindra stavningskontroll på formaterad text för renare design. Förbättra dina dokument med precision och professionalism!
type: docs
weight: 280
url: /sv/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Sant när de formaterade tecknen inte ska stavningskontrolleras.

```csharp
public bool NoProofing { get; set; }
```

## Exempel

Visar hur man förhindrar att text stavningskontrolleras av Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalt sett betonar Microsoft Word stavfel med en ojämn röd understrykning.
// Vi kan avaktivera flaggan "NoProofing" för att skapa en del av texten som
// kringgår stavningskontrollen samtidigt som den inaktiveras helt.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
