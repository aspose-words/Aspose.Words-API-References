---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Gibt an ob Textfelder Fußnoten und Endnoten in die Wortzahlstatistik einbezogen werden sollen.
type: docs
weight: 220
url: /de/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Gibt an, ob Textfelder, Fußnoten und Endnoten in die Wortzahlstatistik einbezogen werden sollen.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

### Beispiele

Zeigt, wie Textfelder, Fußnoten und Endnoten in die Wortzahlstatistik einbezogen oder ausgeschlossen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Standardmäßig ist die Option auf „false“ gesetzt.
doc.UpdateWordCount();
// Wörter zählen ohne Textfelder, Fußnoten und Endnoten.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Wörter zählen mit Textfeldern, Fußnoten und Endnoten.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


