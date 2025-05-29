---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words für .NET
description: Optimieren Sie die Wortanzahl Ihres Dokuments mit der Eigenschaft „IncludeTextboxesFootnotesEndnotesInStat“. Steuern Sie Textfelder, Fußnoten und Endnoten mühelos!
type: docs
weight: 230
url: /de/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Gibt an, ob Textfelder, Fußnoten und Endnoten in die Wortzählstatistik einbezogen werden sollen.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Beispiele

Zeigt, wie Textfelder, Fußnoten und Endnoten in die Wortzählstatistik einbezogen oder davon ausgeschlossen werden.

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
// Wörter werden mit Textfeldern, Fußnoten und Endnoten gezählt.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
