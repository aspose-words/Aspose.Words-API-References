---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.FootnoteType. Unterscheiden Sie einfach zwischen Fußnoten und Endnoten, um die Formatierung und Übersichtlichkeit Ihres Dokuments zu verbessern.
type: docs
weight: 5020
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

## Bemerkungen

Sowohl Fußnoten als auch Endnoten werden durch Objekte dargestellt, die durch dieFootnote Klasse. Verwenden[`FootnoteType`](../footnote/footnotetype/) um zwischen Fußnoten und Endnoten zu unterscheiden.

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

Zeigt, wie Fußnoten eingefügt und angepasst werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text hinzufügen und mit einer Fußnote darauf verweisen. Diese Fußnote enthält einen kleinen hochgestellten Verweis
// Markieren Sie nach dem Text, auf den verwiesen wird, und erstellen Sie einen Eintrag unter dem Haupttext am unteren Seitenrand.
// Dieser Eintrag enthält das Referenzzeichen und den Referenztext der Fußnote,
// die wir an die Methode „InsertFootnote“ des Dokument-Generators übergeben.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wenn diese Eigenschaft auf "true" gesetzt ist, dann ist das Referenzzeichen unserer Fußnote
// wird sein Index unter allen Fußnoten des Abschnitts sein.
// Dies ist die erste Fußnote, daher lautet das Referenzzeichen „1“.
Assert.True(footnote.IsAuto);

    // Wir können den Dokumentgenerator in die Fußnote verschieben, um den Referenztext zu bearbeiten.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wir können ein benutzerdefiniertes Referenzzeichen festlegen, das die Fußnote anstelle ihrer Indexnummer verwendet.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ein Lesezeichen mit dem Flag "IsAuto" auf true wird immer noch seinen tatsächlichen Index anzeigen
// Auch wenn vorherige Lesezeichen benutzerdefinierte Referenzzeichen anzeigen, ist das Referenzzeichen dieses Lesezeichens eine „3“.
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)
