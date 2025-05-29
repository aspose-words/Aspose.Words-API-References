---
title: Footnote.IsAuto
linktitle: IsAuto
articleTitle: IsAuto
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsAuto-Eigenschaft für Fußnoten, die eine nahtlose automatische Nummerierung oder benutzerdefinierte Referenzzeichen für eine verbesserte Übersichtlichkeit und Organisation des Dokuments ermöglicht.
type: docs
weight: 40
url: /de/net/aspose.words.notes/footnote/isauto/
---
## Footnote.IsAuto property

Enthält einen Wert, der angibt, ob es sich um eine automatisch nummerierte Fußnote oder eine Fußnote mit benutzerdefiniertem Referenzzeichen handelt.

```csharp
public bool IsAuto { get; set; }
```

## Bemerkungen

[`ReferenceMark`](../referencemark/) mit einer leeren Zeichenfolge initialisiert, wenn`IsAuto` eingestellt auf`FALSCH` .

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
