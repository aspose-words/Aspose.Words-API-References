---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FindReplaceOptions IgnoreFootnotes“, um Fußnoten in Ihren Dokumenten einfach zu verwalten. Steigern Sie die Bearbeitungseffizienz mit diesem einfachen Schalter!
type: docs
weight: 90
url: /de/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Beispiele

Zeigt, wie Fußnoten während einer Suchen-und-Ersetzen-Operation ignoriert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Setzen Sie das Flag "IgnoreFootnotes" auf "true", um die Suchen-und-Ersetzen-Funktion zu erhalten
// Operation zum Ignorieren von Text in Fußnoten.
// Setzen Sie das Flag "IgnoreFootnotes" auf "false", um die Funktion "Suchen und Ersetzen" zu erhalten.
// Operation, um auch in Fußnoten nach Text zu suchen.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
