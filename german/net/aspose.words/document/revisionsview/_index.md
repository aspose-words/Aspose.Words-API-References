---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words für .NET
description: Document RevisionsView eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob mit der Originalversion oder der überarbeiteten Version eines Dokuments gearbeitet werden soll in C#.
type: docs
weight: 360
url: /de/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob mit der Originalversion oder der überarbeiteten Version eines Dokuments gearbeitet werden soll.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## Bemerkungen

Der Standardwert ist .

## Beispiele

Zeigt, wie zwischen der überarbeiteten und der Originalansicht eines Dokuments gewechselt wird.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Das Dokumentobjekt so anzeigen, als ob alle Revisionen akzeptiert würden. Unterstützt derzeit Listenbezeichnungen.
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
