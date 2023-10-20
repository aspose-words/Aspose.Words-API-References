---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words for .NET
description: Document RevisionsView mülk. Bir belgenin orijinal sürümüyle mi yoksa revize edilmiş sürümüyle mi çalışılacağını belirten bir değer alır veya ayarlar C#'da.
type: docs
weight: 360
url: /tr/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Bir belgenin orijinal sürümüyle mi yoksa revize edilmiş sürümüyle mi çalışılacağını belirten bir değer alır veya ayarlar.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## Notlar

Varsayılan değer: .

## Örnekler

Bir belgenin revize edilmiş görünümü ile orijinal görünümü arasında nasıl geçiş yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Belge nesnesini tüm revizyonlar kabul edilmiş gibi görüntüleyin. Şu anda liste etiketlerini desteklemektedir.
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
