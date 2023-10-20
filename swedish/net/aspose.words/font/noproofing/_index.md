---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words för .NET
description: Font NoProofing fast egendom. Sant när de formaterade tecknen inte ska stavningskontrolleras i C#.
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

Visar hur du förhindrar att text stavningskontrolleras av Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalt betonar Microsoft Word stavfel med en ojämn röd underlinje.
// Vi kan avaktivera "NoProofing"-flaggan för att skapa en del av text som
// går förbi stavningskontrollen samtidigt som den inaktiveras helt.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
