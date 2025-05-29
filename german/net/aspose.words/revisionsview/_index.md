---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.RevisionsView, um einfach zwischen Original- und überarbeiteten Dokumentversionen zu wählen und so die Bearbeitung und Zusammenarbeit zu optimieren.
type: docs
weight: 5550
url: /de/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Ermöglicht die Angabe, ob mit der Originalversion oder der überarbeiteten Version eines Dokuments gearbeitet werden soll.

```csharp
public enum RevisionsView
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Original | `0` | Gibt die Originalversion eines Dokuments an. |
| Final | `1` | Gibt die überarbeitete Version eines Dokuments an. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
