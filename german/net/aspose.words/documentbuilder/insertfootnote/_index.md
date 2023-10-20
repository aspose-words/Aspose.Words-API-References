---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words für .NET
description: DocumentBuilder InsertFootnote methode. Fügt eine Fußnote oder Endnote in das Dokument ein in C#.
type: docs
weight: 330
url: /de/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Fügt eine Fußnote oder Endnote in das Dokument ein.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteType | FootnoteType | Gibt an, ob eine Fußnote oder eine Endnote eingefügt werden soll. |
| footnoteText | String | Gibt den Text der Fußnote an. |

### Rückgabewert

Gibt ein gerade erstelltes Fußnotenobjekt zurück.

## Beispiele

Zeigt, wie Text mit einer Fußnote und einer Endnote referenziert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie etwas Text ein und markieren Sie ihn mit einer Fußnote, wobei die IsAuto-Eigenschaft standardmäßig auf „true“ gesetzt ist.
// damit die im Fließtext angezeigte Markierung automatisch bei „1“ nummeriert wird,
// und die Fußnote erscheint am Ende der Seite.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Fügen Sie mehr Text ein und markieren Sie ihn mit einer Endnote mit einem benutzerdefinierten Referenzzeichen.
// die anstelle der Zahl „2“ verwendet wird und „IsAuto“ auf „false“ setzt.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fußnoten erscheinen immer am Ende des referenzierten Textes,
// Daher hat dieser Seitenumbruch keinen Einfluss auf die Fußnote.
// Endnoten hingegen stehen immer am Ende des Dokuments
// damit dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Siehe auch

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Fügt eine Fußnote oder Endnote in das Dokument ein.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteType | FootnoteType | Gibt an, ob eine Fußnote oder eine Endnote eingefügt werden soll. |
| footnoteText | String | Gibt den Text der Fußnote an. |
| referenceMark | String | Gibt das benutzerdefinierte Referenzzeichen der Fußnote an. |

### Rückgabewert

Gibt ein gerade erstelltes Fußnotenobjekt zurück.

## Beispiele

Zeigt, wie Text mit einer Fußnote und einer Endnote referenziert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie etwas Text ein und markieren Sie ihn mit einer Fußnote, wobei die IsAuto-Eigenschaft standardmäßig auf „true“ gesetzt ist.
// damit die im Fließtext angezeigte Markierung automatisch bei „1“ nummeriert wird,
// und die Fußnote erscheint am Ende der Seite.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Fügen Sie mehr Text ein und markieren Sie ihn mit einer Endnote mit einem benutzerdefinierten Referenzzeichen.
// die anstelle der Zahl „2“ verwendet wird und „IsAuto“ auf „false“ setzt.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fußnoten erscheinen immer am Ende des referenzierten Textes,
// Daher hat dieser Seitenumbruch keinen Einfluss auf die Fußnote.
// Endnoten hingegen stehen immer am Ende des Dokuments
// damit dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Siehe auch

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
