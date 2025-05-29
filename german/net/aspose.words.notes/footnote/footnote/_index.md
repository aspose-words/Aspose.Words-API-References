---
title: Footnote
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos ansprechende Fußnoten mit unserem Fußnoten-Editor. Verbessern Sie die Klarheit und Professionalität Ihrer Inhalte mit nur wenigen Klicks!
type: docs
weight: 10
url: /de/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Initialisiert eine Instanz des[`Footnote`](../) Klasse.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |
| footnoteType | FootnoteType | A[`FootnoteType`](../footnotetype/) value , der angibt, ob es sich um eine Fußnote oder eine Endnote handelt. |

## Bemerkungen

Wann[`Footnote`](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und[`ParentNode`](../../../aspose.words/node/parentnode/) Ist`null`.

Anhängen[`Footnote`](../) zur Dokumentenverwendung[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) oder[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) auf den Absatz, in den Sie die Fußnote einfügen möchten.

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
