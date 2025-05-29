---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der InsertFootnote-Methode von DocumentBuilder – fügen Sie einfach Fußnoten oder Endnoten hinzu, um für mehr Klarheit und Professionalität zu sorgen.
type: docs
weight: 340
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

Zeigt, wie Sie mit einer Fußnote und einer Endnote auf Text verweisen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie Text ein und markieren Sie ihn mit einer Fußnote, wobei die Eigenschaft IsAuto standardmäßig auf „true“ gesetzt ist.
// so dass die Markierung im Haupttext automatisch mit "1" nummeriert wird,
// und die Fußnote wird unten auf der Seite angezeigt.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Fügen Sie weiteren Text ein und markieren Sie ihn mit einer Endnote mit einem benutzerdefinierten Referenzzeichen,
// die anstelle der Zahl „2“ verwendet wird und „IsAuto“ auf „false“ setzt.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fußnoten erscheinen immer am Ende des referenzierten Textes,
// daher hat dieser Seitenumbruch keine Auswirkungen auf die Fußnote.
// Andererseits stehen Endnoten immer am Ende des Dokuments
// sodass dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
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

Zeigt, wie Sie mit einer Fußnote und einer Endnote auf Text verweisen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie Text ein und markieren Sie ihn mit einer Fußnote, wobei die Eigenschaft IsAuto standardmäßig auf „true“ gesetzt ist.
// so dass die Markierung im Haupttext automatisch mit "1" nummeriert wird,
// und die Fußnote wird unten auf der Seite angezeigt.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Fügen Sie weiteren Text ein und markieren Sie ihn mit einer Endnote mit einem benutzerdefinierten Referenzzeichen,
// die anstelle der Zahl „2“ verwendet wird und „IsAuto“ auf „false“ setzt.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fußnoten erscheinen immer am Ende des referenzierten Textes,
// daher hat dieser Seitenumbruch keine Auswirkungen auf die Fußnote.
// Andererseits stehen Endnoten immer am Ende des Dokuments
// sodass dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Siehe auch

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
