---
title: Document.RevisionsView
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. Bir belgenin orijinal mi yoksa gözden geçirilmiş sürümüyle mi çalışılacağını belirten bir değer alır veya ayarlar.
type: docs
weight: 340
url: /tr/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Bir belgenin orijinal mi yoksa gözden geçirilmiş sürümüyle mi çalışılacağını belirten bir değer alır veya ayarlar.

```csharp
public RevisionsView RevisionsView { get; set; }
```

### Notlar

Varsayılan değer .

### Örnekler

Bir belgenin gözden geçirilmiş ve orijinal görünümü arasında nasıl geçiş yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Belge nesnesini tüm revizyonlar kabul edilmiş gibi görüntüleyin. Şu anda liste etiketlerini destekler.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Ayrıca bakınız

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


