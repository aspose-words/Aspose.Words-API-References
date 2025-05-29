---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words för .NET
description: Upptäck hur du optimerar teckenavståndet i ditt dokument med egenskapen JustificationMode. Förbättra läsbarheten och presentationen utan ansträngning!
type: docs
weight: 240
url: /sv/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Hämtar eller ställer in justeringen av teckenavståndet för ett dokument.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Exempel

Visar hur man hanterar teckenavståndskontroll.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Se även

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
