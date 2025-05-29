---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words für .NET
description: Entdecken Sie die FootnoteType-Eigenschaft und identifizieren Sie Fußnoten oder Endnoten in Ihren Dokumenten ganz einfach für mehr Klarheit und Organisation.
type: docs
weight: 30
url: /de/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Gibt einen Wert zurück, der angibt, ob es sich um eine Fußnote oder eine Endnote handelt.

```csharp
public FootnoteType FootnoteType { get; }
```

## Beispiele

Zeigt den Unterschied zwischen Fußnoten und Endnoten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend sind zwei Möglichkeiten aufgeführt, nummerierte Referenzen an den Text anzuhängen. Beide Referenzen fügen eine
// kleines hochgestelltes Referenzzeichen an der Stelle, an der wir sie einfügen.
// Das Referenzzeichen ist standardmäßig die Indexnummer der Referenz unter allen Referenzen im Dokument.
// Jeder Verweis erzeugt ebenfalls einen Eintrag, der das gleiche Verweiszeichen wie im Fließtext trägt.
// und Referenztext, den wir an die Methode „InsertFootnote“ des Dokument-Generators übergeben.
// 1 - Eine Fußnote, deren Eintrag auf derselben Seite erscheint wie der Text, auf den sie verweist:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - Eine Endnote, deren Eintrag am Ende des Dokuments erscheint:
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(FootnoteType.Footnote, footnote.FootnoteType);
Assert.AreEqual(FootnoteType.Endnote, endnote.FootnoteType);

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### Siehe auch

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
