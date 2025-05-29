---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: .NET için Aspose.Words
description: Belgelerinizdeki referans işaretlerinin tam metnine erişmek, netliği ve organizasyonu artırmak için Dipnot ActualReferenceMark özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

Bu dipnot için belgede görüntülenen referans işaretinin gerçek metnini alır.

```csharp
public string ActualReferenceMark { get; }
```

## Notlar

Bu özelliğin değerlerini başlangıçta belgenin tüm başvuru işaretleri için doldurmak veya başvuru işaretlerini etkileyebilecek belgedeki değişikliklerden sonra değerleri güncellemek için öğesini yürütmeniz gerekir.[`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) method. Alanlar güncelleniyor ([`UpdateFields`](../../../aspose.words/document/updatefields/) ) doğru sonucu elde etmek için gerekli olabilir.

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

* class [Footnote](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
