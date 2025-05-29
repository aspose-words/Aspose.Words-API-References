---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: .NET için Aspose.Words
description: Belge revizyonlarını zahmetsizce yönetin! Sorunsuz işbirliği ve gelişmiş üretkenlik için orijinal veya güncellenmiş sürümler arasında seçim yapın.
type: docs
weight: 380
url: /tr/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Bir belgenin orijinal veya revize edilmiş sürümüyle çalışılıp çalışılmayacağını belirten bir değer alır veya ayarlar.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## Notlar

Varsayılan değer: .

## Örnekler

Bir belgenin düzeltilmiş ve orijinal görünümü arasında nasıl geçiş yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Belge nesnesini tüm revizyonlar kabul edilmiş gibi görüntüle. Şu anda liste etiketlerini destekliyor.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Ayrıca bakınız

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
