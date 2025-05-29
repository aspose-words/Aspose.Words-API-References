---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Belgenizin biçimlendirmesini geliştirerek, türüne göre özelleştirilmiş DipnotAyırıcılarını kolayca almak için DipnotAyırıcıKoleksiyonu Öğesi özelliğine erişin.
type: docs
weight: 20
url: /tr/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

Birini alır[`FootnoteSeparator`](../../footnoteseparator/) belirtilen türde.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## Notlar

Geri Döndürür`hükümsüz` Belirtilen türdeki dipnot/sonnot ayırıcısı bulunamazsa.

## Örnekler

Dipnot ayırıcı formatının nasıl yönetileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Dipnot ayırıcısını hizala.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Ayrıca bakınız

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
