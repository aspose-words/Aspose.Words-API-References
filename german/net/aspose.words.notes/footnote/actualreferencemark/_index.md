---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Footnote ActualReferenceMark“, um auf den genauen Text der Referenzzeichen in Ihren Dokumenten zuzugreifen und so die Klarheit und Organisation zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

Ruft den tatsächlichen Text des Referenzzeichens ab, das im Dokument für diese Fußnote angezeigt wird.

```csharp
public string ActualReferenceMark { get; }
```

## Bemerkungen

Um die Werte dieser Eigenschaft zunächst für alle Referenzmarken des Dokuments zu füllen oder um die Werte nach Änderungen im Dokument, die die Referenzmarken beeinflussen könnten, zu aktualisieren, müssen Sie den [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) method. Felder aktualisieren ([`UpdateFields`](../../../aspose.words/document/updatefields/) ) kann ebenfalls erforderlich sein, um das richtige Ergebnis zu erhalten.

## Beispiele

Zeigt, wie man ein tatsächliches Fußnotenreferenzzeichen erhält.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### Siehe auch

* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
