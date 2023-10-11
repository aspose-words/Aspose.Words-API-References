---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder fast egendom. Returnerar Sann om markören är i slutet av en strukturerad dokumenttagg.
type: docs
weight: 120
url: /sv/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

Returnerar **Sann** om markören är i slutet av en strukturerad dokumenttagg.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
```

### Exempel

Visar hur man flyttar markören för DocumentBuilder inuti en strukturerad dokumenttagg.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Det finns flera sätt att flytta markören:
// 1 - Flytta till det första tecknet i strukturerad dokumenttagg efter index.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Flytta till det första tecknet i strukturerade dokument taggar för objekt.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Flytta till slutet av den andra strukturerade dokumenttaggen.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// Hämta för närvarande vald strukturerad dokumenttagg.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


