---
title: Footnote.Footnote
second_title: Aspose.Words für .NET-API-Referenz
description: Footnote constructeur. Initialisiert eine Instanz von Fußnote Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Initialisiert eine Instanz von **Fußnote** Klasse.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Besitzerdokument. |
| footnoteType | FootnoteType | EIN[`FootnoteType`](../footnotetype/) value , der angibt, ob es sich um eine Fuß- oder Endnote handelt. |

### Bemerkungen

Wann **Fußnote** erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und **Elternknoten** ist Null.

Anhängen **Fußnote** zum Dokument verwenden Sie InsertAfter oder InsertBefore in dem Absatz, in dem Sie die Fußnote einfügen möchten.

### Beispiele

Zeigt, wie Fußnoten eingefügt und angepasst werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text hinzufügen und mit einer Fußnote darauf verweisen. Diese Fußnote platziert einen kleinen hochgestellten Verweis
// Markieren Sie nach dem Text, auf den es verweist, und erstellen Sie einen Eintrag unter dem Haupttext unten auf der Seite.
// Dieser Eintrag enthält das Referenzzeichen der Fußnote und den Referenztext,
// die wir an die "InsertFootnote"-Methode des Dokumenterstellers übergeben.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wenn diese Eigenschaft auf "true" gesetzt ist, dann das Referenzzeichen unserer Fußnote
// wird sein Index unter allen Fußnoten des Abschnitts sein.
// Dies ist die erste Fußnote, also ist die Referenzmarke "1".
Assert.True(footnote.IsAuto);

// Wir können den Document Builder in die Fußnote verschieben, um seinen Referenztext zu bearbeiten. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wir können eine benutzerdefinierte Referenzmarke setzen, die die Fußnote anstelle ihrer Indexnummer verwendet.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ein Lesezeichen, bei dem das Flag "IsAuto" auf "true" gesetzt ist, zeigt immer noch seinen echten Index
// Auch wenn frühere Lesezeichen benutzerdefinierte Referenzzeichen anzeigen, ist das Referenzzeichen dieses Lesezeichens eine "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Siehe auch

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../footnote/)
* Montage [Aspose.Words](../../../)


