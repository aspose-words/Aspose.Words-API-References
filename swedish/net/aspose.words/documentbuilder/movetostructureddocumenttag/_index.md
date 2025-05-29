---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words för .NET
description: Navigera enkelt till strukturerade dokumenttaggar med DocumentBuilder-metoden MoveToStructuredDocumentTag, vilket förbättrar din dokumentredigeringseffektivitet.
type: docs
weight: 620
url: /sv/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Flyttar markören till en strukturerad dokumenttagg i det aktuella avsnittet.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | Indexet för den strukturerade dokumenttaggen som ska flyttas till. |
| characterIndex | Int32 | Index för tecknet inuti den strukturerade dokumenttaggen. Ett negativt värde låter dig ange en position från slutet av den strukturerade dokumenttaggen. Använd -1 för att flytta till slutet av den strukturerade dokumenttaggen. Om den strukturerade dokumenttaggen är på blocknivå och du vill flytta markören till slutet av dess sista stycke, ange -2. |

## Anmärkningar

Navigeringen utförs inom den aktuella artikeln i det aktuella avsnittet. Det vill säga, om du flyttade markören till den primära rubriken i det första avsnittet, så*structuredDocumentTagIndex* angav indexet för den strukturerade dokumenttaggen inuti rubriken i det avsnittet.

När*structuredDocumentTagIndex* är större än eller lika med 0, anger den ett index från början av avsnittet där 0 är den första taggen för strukturerat dokument. När *structuredDocumentTagIndex*är mindre än 0, specificerade den ett index från slutet av avsnittet där -1 är den sista taggen för strukturerat dokument.

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

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Flyttar markören till den strukturerade dokumenttaggen.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Den strukturerade dokumenttagg att flytta till. |
| characterIndex | Int32 | Index för tecknet inuti den strukturerade dokumenttaggen. Ett negativt värde låter dig ange en position från slutet av den strukturerade dokumenttaggen. Använd -1 för att flytta till slutet av den strukturerade dokumenttaggen. Om den strukturerade dokumenttaggen är på blocknivå och du vill flytta markören till slutet av dess sista stycke, ange -2. |

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

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
