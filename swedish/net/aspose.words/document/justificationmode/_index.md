---
title: Document.JustificationMode
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Hämtar eller ställer in teckenavståndsjusteringen för ett dokument.
type: docs
weight: 230
url: /sv/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Hämtar eller ställer in teckenavståndsjusteringen för ett dokument.

```csharp
public JustificationMode JustificationMode { get; set; }
```

### Exempel

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
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


