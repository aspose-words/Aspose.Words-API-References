---
title: FindReplaceOptions.ApplyParagraphFormat
linktitle: ApplyParagraphFormat
articleTitle: ApplyParagraphFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die ApplyParagraphFormat-Eigenschaft in FindReplaceOptions für eine nahtlose Absatzformatierung in Ihren Dokumenten. Optimieren Sie Ihre Inhalte mühelos!
type: docs
weight: 30
url: /de/net/aspose.words.replacing/findreplaceoptions/applyparagraphformat/
---
## FindReplaceOptions.ApplyParagraphFormat property

Absatzformatierung auf neuen Inhalt angewendet.

```csharp
public ParagraphFormat ApplyParagraphFormat { get; }
```

## Beispiele

Zeigt, wie Sie Absätzen, in denen eine Suchen-und-Ersetzen-Operation Übereinstimmungen gefunden hat, Formatierungen hinzufügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie die Eigenschaft „Alignment“ auf „ParagraphAlignment.Right“, um jeden Absatz rechtsbündig auszurichten
// das eine Übereinstimmung enthält, die durch die Such- und Ersetzungsoperation gefunden wird.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Ersetzen Sie jeden Punkt direkt vor einem Absatzumbruch durch ein Ausrufezeichen.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Siehe auch

* class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
