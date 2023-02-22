---
title: Footnote.FootnoteType
second_title: Aspose.Words für .NET-API-Referenz
description: Footnote eigendom. Gibt einen Wert zurück der angibt ob es sich um eine Fuß oder Endnote handelt.
type: docs
weight: 20
url: /de/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Gibt einen Wert zurück, der angibt, ob es sich um eine Fuß- oder Endnote handelt.

```csharp
public FootnoteType FootnoteType { get; }
```

### Beispiele

Zeigt den Unterschied zwischen Fußnoten und Endnoten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Im Folgenden finden Sie zwei Möglichkeiten, dem Text nummerierte Referenzen hinzuzufügen. Diese beiden Referenzen werden a hinzufügen
// kleine hochgestellte Referenzmarke an der Stelle, an der wir sie einfügen.
// Die Referenzmarke ist standardmäßig die Indexnummer der Referenz unter allen Referenzen im Dokument.
// Jede Referenz erstellt auch einen Eintrag, der die gleiche Referenzmarke wie im Fließtext hat
// und Referenztext, den wir an die "InsertFootnote"-Methode des Dokumenterstellers übergeben.
// 1 - Eine Fußnote, deren Eintrag auf derselben Seite erscheint wie der Text, auf den er verweist:
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
* namensraum [Aspose.Words.Notes](../../footnote/)
* Montage [Aspose.Words](../../../)


