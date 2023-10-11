---
title: DocumentBuilder.CurrentStructuredDocumentTag
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder fast egendom. Hämtar den strukturerade dokumenttaggen som för närvarande är vald i dennaDocumentBuilder .
type: docs
weight: 80
url: /sv/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Hämtar den strukturerade dokumenttaggen som för närvarande är vald i denna[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
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

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


