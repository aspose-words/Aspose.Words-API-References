---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words für .NET
description: Aspose.Words.RevisionsView opsomming. Ermöglicht die Angabe ob mit der Originalversion oder der überarbeiteten Version eines Dokuments gearbeitet werden soll in C#.
type: docs
weight: 4810
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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
