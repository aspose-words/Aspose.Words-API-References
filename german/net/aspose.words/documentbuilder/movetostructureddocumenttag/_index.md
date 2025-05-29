---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words für .NET
description: Navigieren Sie mühelos zu strukturierten Dokument-Tags mit der DocumentBuilder MoveToStructuredDocumentTag-Methode und steigern Sie so die Effizienz Ihrer Dokumentbearbeitung.
type: docs
weight: 620
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
| characterIndex | Int32 | Der Index des Zeichens innerhalb des Tags für strukturierte Dokumente. Mit einem negativen Wert können Sie eine Position vom Ende des Tags für strukturierte Dokumente angeben. Verwenden Sie -1, um an das Ende des Tags für strukturierte Dokumente zu gelangen. Wenn sich das Tag für strukturierte Dokumente auf Blockebene befindet und Sie den Cursor an das Ende des letzten Absatzes bewegen möchten, geben Sie -2 an. |

## Bemerkungen

Die Navigation erfolgt innerhalb der aktuellen Story des aktuellen Abschnitts. Das heißt, wenn Sie den Cursor auf die primäre Überschrift des ersten Abschnitts bewegt haben, dann*structuredDocumentTagIndex* gibt den Index des strukturierten Dokument-Tags innerhalb der Kopfzeile dieses Abschnitts an.

Wann*structuredDocumentTagIndex* größer oder gleich 0 ist, gibt es einen Index vom Anfang des Abschnitts an, wobei 0 das erste strukturierte Dokument-Tag ist. Wenn *structuredDocumentTagIndex*kleiner als 0 ist, wird ein Index vom Ende des Abschnitts angegeben, wobei -1 das letzte strukturierte Dokument-Tag ist.

## Beispiele

Zeigt, wie der Cursor von DocumentBuilder innerhalb eines strukturierten Dokument-Tags bewegt wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, den Cursor zu bewegen:
// 1 – Wechseln Sie nach Index zum ersten Zeichen des strukturierten Dokument-Tags.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 – Wechseln Sie zum ersten Zeichen des strukturierten Dokument-Tags nach Objekt.
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

Bewegt den Cursor zum strukturierten Dokument-Tag.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Das strukturierte Dokument-Tag, zu dem verschoben werden soll. |
| characterIndex | Int32 | Der Index des Zeichens innerhalb des Tags für strukturierte Dokumente. Mit einem negativen Wert können Sie eine Position vom Ende des Tags für strukturierte Dokumente angeben. Verwenden Sie -1, um an das Ende des Tags für strukturierte Dokumente zu gelangen. Wenn sich das Tag für strukturierte Dokumente auf Blockebene befindet und Sie den Cursor an das Ende des letzten Absatzes bewegen möchten, geben Sie -2 an. |

## Beispiele

Zeigt, wie der Cursor von DocumentBuilder innerhalb eines strukturierten Dokument-Tags bewegt wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, den Cursor zu bewegen:
// 1 – Wechseln Sie nach Index zum ersten Zeichen des strukturierten Dokument-Tags.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 – Wechseln Sie zum ersten Zeichen des strukturierten Dokument-Tags nach Objekt.
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
