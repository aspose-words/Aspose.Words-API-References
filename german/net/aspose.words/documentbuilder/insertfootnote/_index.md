---
title: InsertFootnote
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt eine Fuß- oder Endnote in das Dokument ein.
type: docs
weight: 310
url: /de/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(FootnoteType, string) {#insertfootnote}

Fügt eine Fuß- oder Endnote in das Dokument ein.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteType | FootnoteType | Gibt an, ob eine Fußnote oder eine Endnote eingefügt werden soll. |
| footnoteText | String | Gibt den Text der Fußnote an. |

### Rückgabewert

Gibt ein Fußnotenobjekt zurück, das gerade erstellt wurde.

### Beispiele

Zeigt, wie auf Text mit einer Fußnote und einer Endnote verwiesen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie etwas Text ein und markieren Sie ihn mit einer Fußnote, wobei die IsAuto-Eigenschaft standardmäßig auf "true" gesetzt ist,
// also wird die Markierung im Fließtext automatisch mit "1" nummeriert,
// und die Fußnote erscheint unten auf der Seite.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Fügen Sie mehr Text ein und markieren Sie ihn mit einer Endnote mit einer benutzerdefinierten Referenzmarke,
// die anstelle der Zahl "2" verwendet wird und "IsAuto" auf "false" setzt.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fußnoten erscheinen immer am Ende ihres referenzierten Textes,
// also wirkt sich dieser Seitenumbruch nicht auf die Fußnote aus.
// Andererseits stehen Endnoten immer am Ende des Dokuments
// damit dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Siehe auch

* class [Footnote](../../../aspose.words.notes/footnote)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype)
* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

---

## InsertFootnote(FootnoteType, string, string) {#insertfootnote_1}

Fügt eine Fuß- oder Endnote in das Dokument ein.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteType | FootnoteType | Gibt an, ob eine Fußnote oder eine Endnote eingefügt werden soll. |
| footnoteText | String | Gibt den Text der Fußnote an. |
| referenceMark | String | Gibt das benutzerdefinierte Referenzzeichen der Fußnote an. |

### Rückgabewert

Gibt ein Fußnotenobjekt zurück, das gerade erstellt wurde.

### Beispiele

Zeigt, wie auf Text mit einer Fußnote und einer Endnote verwiesen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie etwas Text ein und markieren Sie ihn mit einer Fußnote, wobei die IsAuto-Eigenschaft standardmäßig auf "true" gesetzt ist,
// also wird die Markierung im Fließtext automatisch mit "1" nummeriert,
// und die Fußnote erscheint unten auf der Seite.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Fügen Sie mehr Text ein und markieren Sie ihn mit einer Endnote mit einer benutzerdefinierten Referenzmarke,
// die anstelle der Zahl "2" verwendet wird und "IsAuto" auf "false" setzt.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fußnoten erscheinen immer am Ende ihres referenzierten Textes,
// also wirkt sich dieser Seitenumbruch nicht auf die Fußnote aus.
// Andererseits stehen Endnoten immer am Ende des Dokuments
// damit dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Siehe auch

* class [Footnote](../../../aspose.words.notes/footnote)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype)
* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->