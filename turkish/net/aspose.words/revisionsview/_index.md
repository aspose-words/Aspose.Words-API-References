---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: .NET için Aspose.Words
description: Düzenleme ve işbirliğini kolaylaştırmak için orijinal ve revize edilmiş belge sürümleri arasında kolayca seçim yapmak üzere Aspose.Words.RevisionsView enum'unu keşfedin.
type: docs
weight: 5550
url: /tr/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Bir belgenin orijinal mi yoksa revize edilmiş sürümüyle mi çalışılacağını belirtmenizi sağlar.

```csharp
public enum RevisionsView
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Original | `0` | Belgenin orijinal sürümünü belirtir. |
| Final | `1` | Bir belgenin gözden geçirilmiş sürümünü belirtir. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
