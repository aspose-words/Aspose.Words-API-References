---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words für .NET
description: DocumentBuilder MoveToStructuredDocumentTag methode. Bewegt den Cursor zu einem strukturierten DokumentTag im aktuellen Abschnitt in C#.
type: docs
weight: 580
url: /de/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Bewegt den Cursor zu einem strukturierten Dokument-Tag im aktuellen Abschnitt.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | Der Index des strukturierten Dokumenttags, zu dem verschoben werden soll. |
| characterIndex | Int32 | Der Index des Zeichens innerhalb des strukturierten Dokument-Tags. Mit einem negativen Wert können Sie eine Position ab dem Ende des strukturierten Dokument-Tags angeben. Verwenden Sie -1, um zum Ende des strukturierten Dokument-Tags zu verschieben. Wenn sich das Tag des strukturierten Dokuments auf Blockebene befindet und Sie den Cursor an das Ende des letzten Absatzes bewegen möchten, geben Sie -2 an. |

## Bemerkungen

Die Navigation erfolgt innerhalb der aktuellen Story des aktuellen Abschnitts. Das heißt, wenn Sie den -Cursor auf die primäre Kopfzeile des ersten Abschnitts verschoben haben, dann*structuredDocumentTagIndex* gab den Index des strukturierten Dokument-Tags in der Kopfzeile dieses Abschnitts an.

Wann*structuredDocumentTagIndex* größer oder gleich 0 ist, gibt es einen index vom Anfang des Abschnitts an, wobei 0 das erste Tag des strukturierten Dokuments ist. Wann *structuredDocumentTagIndex* kleiner als 0 ist, wird ein Index vom Ende des Abschnitts angegeben, wobei -1 das letzte Tag des strukturierten Dokuments ist.

## Beispiele

Zeigt, wie der Cursor von DocumentBuilder innerhalb eines strukturierten Dokument-Tags bewegt wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, den Cursor zu bewegen:
// 1 – Nach Index zum ersten Zeichen des strukturierten Dokument-Tags wechseln.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 – Zum ersten Zeichen des strukturierten Dokuments wechseln, Tag für Objekt.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 – Zum Ende des zweiten strukturierten Dokument-Tags wechseln.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// Aktuell ausgewähltes strukturiertes Dokument-Tag abrufen.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Bewegt den Cursor zum Tag des strukturierten Dokuments.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Das strukturierte Dokument-Tag, zu dem verschoben werden soll. |
| characterIndex | Int32 | Der Index des Zeichens innerhalb des strukturierten Dokument-Tags. Mit einem negativen Wert können Sie eine Position ab dem Ende des strukturierten Dokument-Tags angeben. Verwenden Sie -1, um zum Ende des strukturierten Dokument-Tags zu verschieben. Wenn sich das Tag des strukturierten Dokuments auf Blockebene befindet und Sie den Cursor an das Ende des letzten Absatzes bewegen möchten, geben Sie -2 an. |

## Beispiele

Zeigt, wie der Cursor von DocumentBuilder innerhalb eines strukturierten Dokument-Tags bewegt wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, den Cursor zu bewegen:
// 1 – Nach Index zum ersten Zeichen des strukturierten Dokument-Tags wechseln.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 – Zum ersten Zeichen des strukturierten Dokuments wechseln, Tag für Objekt.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 – Zum Ende des zweiten strukturierten Dokument-Tags wechseln.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// Aktuell ausgewähltes strukturiertes Dokument-Tag abrufen.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
