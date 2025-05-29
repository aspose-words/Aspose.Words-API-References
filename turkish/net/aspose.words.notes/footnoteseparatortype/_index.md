---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: .NET için Aspose.Words
description: Dipnot ve sonnot ayırıcılarını özelleştirmek, belge biçimlendirmesini ve okunabilirliğini geliştirmek için Aspose.Words.FootnoteSeparatorType enum'unu keşfedin.
type: docs
weight: 5010
url: /tr/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

Dipnot/sonnot ayırıcısının türünü belirtir.

```csharp
public enum FootnoteSeparatorType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| FootnoteSeparator | `0` | Ana metin ile dipnot metni arasındaki ayırıcı. |
| FootnoteContinuationSeparator | `1` | Metnin önceki bir sayfadan devam etmesi gerektiğinde, dipnot metninin üstüne basılır. |
| FootnoteContinuationNotice | `2` | Dipnot metninin bir sonraki sayfada devam etmesi gerektiğinde, dipnot metninin altına yazdırılır. |
| EndnoteSeparator | `3` | Ana metin ile son not metni arasındaki ayırıcı. |
| EndnoteContinuationSeparator | `4` | Metnin önceki bir sayfadan devam etmesi gerektiğinde, dipnot metninin üstüne yazdırılır. |
| EndnoteContinuationNotice | `5` | Son not metninin bir sonraki sayfada devam etmesi gerektiğinde, son not metninin altına yazdırılır. |

## Örnekler

Dipnot ayırıcısının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Dipnot ayırıcısını kaldırın.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Dipnot ayırıcı formatının nasıl yönetileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Dipnot ayırıcısını hizala.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
