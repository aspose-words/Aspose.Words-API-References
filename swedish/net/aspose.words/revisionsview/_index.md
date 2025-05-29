---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.RevisionsView enum för att enkelt välja mellan original- och reviderade dokumentversioner för effektiv redigering och samarbete.
type: docs
weight: 5550
url: /sv/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Gör det möjligt att ange om man ska arbeta med originalversionen eller den reviderade versionen av ett dokument.

```csharp
public enum RevisionsView
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Original | `0` | Anger originalversionen av ett dokument. |
| Final | `1` | Anger reviderad version av ett dokument. |

## Exempel

Visar hur man växlar mellan den reviderade och ursprungliga vyn av ett dokument.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Visa dokumentobjektet som om alla revisioner är accepterade. Stöder för närvarande listetiketter.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
