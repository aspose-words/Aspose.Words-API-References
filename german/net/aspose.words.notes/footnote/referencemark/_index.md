---
title: Footnote.ReferenceMark
second_title: Aspose.Words für .NET-API-Referenz
description: Footnote eigendom. Ruft die benutzerdefinierte Referenzmarke ab die für diese Fußnote verwendet werden soll bzw. legt sie fest. Der Standardwert ist leerer String Empty  was bedeutet dass automatisch nummerierte Fußnoten verwendet werden.
type: docs
weight: 50
url: /de/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Ruft die benutzerdefinierte Referenzmarke ab, die für diese Fußnote verwendet werden soll, bzw. legt sie fest. Der Standardwert ist **leerer String** (Empty ), was bedeutet, dass automatisch nummerierte Fußnoten verwendet werden.

```csharp
public string ReferenceMark { get; set; }
```

### Bemerkungen

Wenn diese Eigenschaft auf festgelegt ist **leerer String** (Empty ) oder`Null` , Dann[`IsAuto`](../isauto/) Die Eigenschaft wird automatisch auf gesetzt`WAHR` , , wenn dann etwas anderes eingestellt ist[`IsAuto`](../isauto/) wird eingestellt`FALSCH` .

Das RTF-Format kann nur 1 Symbol als benutzerdefinierte Referenzmarke speichern, daher wird beim Export nur das erste Symbol geschrieben, andere werden verworfen.

### Beispiele

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

* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../footnote/)
* Montage [Aspose.Words](../../../)


