---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words för .NET
description: Hantera dokumentrevisioner enkelt! Välj mellan original- eller uppdaterade versioner för sömlöst samarbete och förbättrad produktivitet.
type: docs
weight: 380
url: /sv/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Hämtar eller anger ett värde som anger om man ska arbeta med originalversionen eller den reviderade versionen av ett dokument.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## Anmärkningar

Standardvärdet är .

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

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
