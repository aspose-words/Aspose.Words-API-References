---
title: Enum FootnoteType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Notes.FootnoteType opsomming. Gibt an ob es sich um eine Fußnote oder eine Endnote handelt.
type: docs
weight: 4300
url: /de/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

Gibt an, ob es sich um eine Fußnote oder eine Endnote handelt.

```csharp
public enum FootnoteType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Footnote | `0` | Das Objekt ist eine Fußnote. |
| Endnote | `1` | Das Objekt ist eine Endnote. |

### Bemerkungen

Sowohl Fußnoten als auch Endnoten werden durch Objekte dargestelltFootnote Klasse. Verwenden[`FootnoteType`](../footnote/footnotetype/) um zwischen Fußnoten und Endnoten zu unterscheiden.

### Beispiele

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

Zeigt, wie Fußnoten eingefügt und angepasst werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text hinzufügen und mit einer Fußnote darauf verweisen. In dieser Fußnote wird ein kleiner hochgestellter Verweis eingefügt
// Markieren Sie nach dem Text, auf den es verweist, und erstellen Sie einen Eintrag unter dem Haupttext am unteren Rand der Seite.
// Dieser Eintrag enthält das Referenzzeichen der Fußnote und den Referenztext,
// die wir an die Methode „InsertFootnote“ des Document Builders übergeben.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wenn diese Eigenschaft auf „true“ gesetzt ist, dann das Referenzzeichen unserer Fußnote
// wird sein Index unter allen Fußnoten des Abschnitts sein.
// Dies ist die erste Fußnote, daher ist die Referenzmarke „1“.
Assert.True(footnote.IsAuto);

 // Wir können den Document Builder in die Fußnote verschieben, um den Referenztext zu bearbeiten.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wir können eine benutzerdefinierte Referenzmarke festlegen, die die Fußnote anstelle ihrer Indexnummer verwendet.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ein Lesezeichen, bei dem das Flag „IsAuto“ auf „true“ gesetzt ist, zeigt weiterhin seinen tatsächlichen Index an
// Auch wenn vorherige Lesezeichen benutzerdefinierte Referenzmarken anzeigen, ist die Referenzmarke dieses Lesezeichens eine „3“.
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)


