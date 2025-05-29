---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words für .NET
description: Aktualisieren Sie mühelos alle Fußnoten und Endnoten in Ihrem Dokument mit der Methode „Document UpdateActualReferenceMarks“ und verbessern Sie so Genauigkeit und Effizienz.
type: docs
weight: 800
url: /de/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

Aktualisiert die[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) Eigenschaft aller Fußnoten und Endnoten im Dokument.

```csharp
public void UpdateActualReferenceMarks()
```

## Bemerkungen

Felder werden aktualisiert ([`UpdateFields`](../updatefields/) ) kann erforderlich sein, um das richtige Ergebnis zu erhalten.

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
