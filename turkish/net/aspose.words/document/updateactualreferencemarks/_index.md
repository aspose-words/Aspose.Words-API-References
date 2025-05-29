---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: .NET için Aspose.Words
description: Belgenizdeki tüm dipnotları ve sonnotları Document UpdateActualReferenceMarks yöntemi ile zahmetsizce güncelleyin, doğruluğu ve verimliliği artırın.
type: docs
weight: 800
url: /tr/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

Günceller[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) belgedeki tüm dipnot ve sonnotların mülkiyeti.

```csharp
public void UpdateActualReferenceMarks()
```

## Notlar

Alanlar güncelleniyor ([`UpdateFields`](../updatefields/) ) doğru sonucu elde etmek için gerekli olabilir.

## Örnekler

Gerçek dipnot referans işaretinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
