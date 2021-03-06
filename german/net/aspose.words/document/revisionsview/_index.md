---
title: RevisionsView
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft einen Wert ab oder legt einen Wert fest der angibt ob mit der ursprünglichen oder der überarbeiteten Version eines Dokuments gearbeitet werden soll.
type: docs
weight: 340
url: /de/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob mit der ursprünglichen oder der überarbeiteten Version eines Dokuments gearbeitet werden soll.

```csharp
public RevisionsView RevisionsView { get; set; }
```

### Bemerkungen

Der Standardwert ist .

### Beispiele

Zeigt, wie Sie zwischen der überarbeiteten und der ursprünglichen Ansicht eines Dokuments wechseln.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Dokumentobjekt anzeigen, als ob alle Revisionen akzeptiert würden. Unterstützt derzeit Listenlabels.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Siehe auch

* enum [RevisionsView](../../revisionsview)
* class [Document](../../document)
* namensraum [Aspose.Words](../../document)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
