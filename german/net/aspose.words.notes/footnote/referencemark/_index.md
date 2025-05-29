---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: Aspose.Words für .NET
description: Passen Sie Ihre Fußnoten mit der ReferenceMark-Eigenschaft an. Setzen Sie einfach eindeutige Markierungen für mehr Übersichtlichkeit und Übersichtlichkeit in Ihren Dokumenten. Verbessern Sie noch heute die Lesbarkeit!
type: docs
weight: 60
url: /de/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Ruft das benutzerdefinierte Referenzzeichen ab/legt es fest, das für diese Fußnote verwendet werden soll. Der Standardwert ist**leere Zeichenfolge** (Empty ), d. h. es werden automatisch nummerierte Fußnoten verwendet.

```csharp
public string ReferenceMark { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft auf**leere Zeichenfolge** (Empty ) oder`null` , Dann[`IsAuto`](../isauto/) Eigenschaft wird automatisch auf`WAHR` , wenn auf etwas anderes eingestellt, dann[`IsAuto`](../isauto/) wird eingestellt auf`FALSCH` .

Im RTF-Format kann nur 1 Symbol als benutzerdefinierte Referenzmarke gespeichert werden, daher wird beim Export nur das erste Symbol geschrieben, alle anderen werden verworfen.

## Beispiele

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

* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
