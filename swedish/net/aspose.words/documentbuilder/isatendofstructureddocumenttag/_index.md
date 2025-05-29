---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
articleTitle: IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilders IsAtEndOfStructuredDocumentTag-egenskap – kontrollera om markören är placerad i slutet av en strukturerad dokumenttagg för effektiv redigering!
type: docs
weight: 120
url: /sv/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

Returer**sann** om markören är i slutet av en strukturerad dokumenttagg.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
```

## Exempel

Visar hur man flyttar markören i DocumentBuilder inuti en strukturerad dokumenttagg.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Det finns flera sätt att flytta markören:
// 1 - Flytta till det första tecknet i den strukturerade dokumenttaggen efter index.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Flytta till det första tecknet i den strukturerade dokumenttaggen efter objekt.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Flytta till slutet av den andra taggen för det strukturerade dokumentet.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Hämta för närvarande vald tagg för strukturerat dokument.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
