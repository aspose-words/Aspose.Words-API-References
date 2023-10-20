---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words for .NET
description: Aspose.Words.RevisionsView Sıralama. Bir belgenin orijinal sürümüyle mi yoksa revize edilmiş sürümüyle mi çalışılacağını belirlemeye olanak tanır C#'da.
type: docs
weight: 4810
url: /tr/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Bir belgenin orijinal sürümüyle mi yoksa revize edilmiş sürümüyle mi çalışılacağını belirlemeye olanak tanır.

```csharp
public enum RevisionsView
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Original | `0` | Bir belgenin orijinal sürümünü belirtir. |
| Final | `1` | Bir belgenin revize edilmiş sürümünü belirtir. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
