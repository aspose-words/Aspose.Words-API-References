---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words für .NET
description: Verwalten Sie Dokumentrevisionen mühelos! Wählen Sie zwischen Original- und aktualisierten Versionen für eine reibungslose Zusammenarbeit und gesteigerte Produktivität.
type: docs
weight: 380
url: /de/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob mit der Originalversion oder der überarbeiteten Version eines Dokuments gearbeitet werden soll.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## Bemerkungen

Der Standardwert ist .

## Beispiele

Zeigt, wie Sie zwischen der überarbeiteten und der Originalansicht eines Dokuments wechseln.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Dokumentobjekt so anzeigen, als ob alle Revisionen akzeptiert wären. Unterstützt derzeit Listenbeschriftungen.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Siehe auch

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
