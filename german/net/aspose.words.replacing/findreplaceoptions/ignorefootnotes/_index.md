---
title: FindReplaceOptions.IgnoreFootnotes
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. Ruft einen booleschen Wert ab oder legt ihn fest der angibt ob Fußnoten ignoriert werden sollen. Der Standardwert istFALSCH .
type: docs
weight: 90
url: /de/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

### Beispiele

Zeigt, wie Fußnoten während eines Suchen-und-Ersetzen-Vorgangs ignoriert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Setzen Sie das Flag „IgnoreFootnotes“ auf „true“, um das Suchen und Ersetzen zu erhalten
// Operation zum Ignorieren von Text in Fußnoten.
// Setzen Sie das Flag „IgnoreFootnotes“ auf „false“, um das Suchen und Ersetzen zu erhalten
// Operation, um auch nach Text in Fußnoten zu suchen.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


