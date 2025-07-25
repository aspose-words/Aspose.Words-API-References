---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words for .NET
description: Effortlessly navigate to structured document tags with the DocumentBuilder MoveToStructuredDocumentTag method, enhancing your document editing efficiency.
type: docs
weight: 620
url: /net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Moves the cursor to a structured document tag in the current section.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | The index of the structured document tag to move to. |
| characterIndex | Int32 | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

## Remarks

The navigation is performed inside the current story of the current section. That is, if you moved the cursor to the primary header of the first section, then *structuredDocumentTagIndex* specified the index of the structured document tag inside that header of that section.

When *structuredDocumentTagIndex* is greater than or equal to 0, it specifies an index from the beginning of the section with 0 being the first structured document tag. When *structuredDocumentTagIndex* is less than 0, it specified an index from the end of the section with -1 being the last structured document tag.

## Examples

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// There is a several ways to move the cursor:
// 1 -  Move to the first character of structured document tag by index.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 -  Move to the first character of structured document tag by object.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.That(tag.GetText().Trim(), Is.EqualTo("R New text.ichText"));

// 3 -  Move to the end of the second structured document tag.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.That(builder.IsAtEndOfStructuredDocumentTag, Is.True);

// Get currently selected structured document tag.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Moves the cursor to the structured document tag.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | The structured document tag to move to. |
| characterIndex | Int32 | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

## Examples

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// There is a several ways to move the cursor:
// 1 -  Move to the first character of structured document tag by index.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 -  Move to the first character of structured document tag by object.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.That(tag.GetText().Trim(), Is.EqualTo("R New text.ichText"));

// 3 -  Move to the end of the second structured document tag.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.That(builder.IsAtEndOfStructuredDocumentTag, Is.True);

// Get currently selected structured document tag.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### See Also

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
