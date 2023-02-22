---
title: Enum RevisionsView
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.RevisionsView opsomming. Ermöglicht festzulegen ob mit der ursprünglichen oder überarbeiteten Version eines Dokuments gearbeitet werden soll.
type: docs
weight: 4550
url: /de/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Ermöglicht festzulegen, ob mit der ursprünglichen oder überarbeiteten Version eines Dokuments gearbeitet werden soll.

```csharp
public enum RevisionsView
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Original | `0` | Gibt die Originalversion eines Dokuments an. |
| Final | `1` | Gibt die überarbeitete Version eines Dokuments an. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


