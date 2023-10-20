---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words för .NET
description: DocumentBuilder MoveToStructuredDocumentTag metod. Flyttar markören till en strukturerad dokumenttagg i det aktuella avsnittet i C#.
type: docs
weight: 580
url: /sv/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Flyttar markören till en strukturerad dokumenttagg i det aktuella avsnittet.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | Indexet för den strukturerade dokumenttaggen att flytta till. |
| characterIndex | Int32 | Indexet för tecknet inuti den strukturerade dokumenttaggen. Ett negativt värde låter dig ange en position från slutet av den strukturerade dokumenttaggen. Använd -1 för att flytta till slutet av den strukturerade dokumenttaggen. Om den strukturerade dokumenttaggen är på blocknivå och du vill flytta markören till slutet av dess sista stycke, ange -2. |

## Anmärkningar

Navigeringen utförs i den aktuella berättelsen i det aktuella avsnittet. Det vill säga, om du flyttade markören till den primära rubriken i det första avsnittet,*structuredDocumentTagIndex* angav indexet för den strukturerade dokumenttaggen inuti den rubriken i det avsnittet.

När*structuredDocumentTagIndex* är större än eller lika med 0, anger den ett index från början av avsnittet där 0 är den första strukturerade dokumenttaggen. When *structuredDocumentTagIndex* är mindre än 0, specificerade det ett index från slutet av sektionen med -1 som den sista strukturerade dokumenttaggen.

## Exempel

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Flyttar markören till den strukturerade dokumenttaggen.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Den strukturerade dokumenttaggen att flytta till. |
| characterIndex | Int32 | Indexet för tecknet inuti den strukturerade dokumenttaggen. Ett negativt värde låter dig ange en position från slutet av den strukturerade dokumenttaggen. Använd -1 för att flytta till slutet av den strukturerade dokumenttaggen. Om den strukturerade dokumenttaggen är på blocknivå och du vill flytta markören till slutet av dess sista stycke, ange -2. |

## Exempel

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
