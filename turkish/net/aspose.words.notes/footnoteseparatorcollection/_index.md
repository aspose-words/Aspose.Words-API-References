---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: .NET için Aspose.Words
description: Belgelerinizdeki dipnot ayırıcılarına kolay erişim için Aspose.Words.Notes.FootnoteSeparatorCollection'ı keşfedin. Belge biçimlendirmenizi bugün geliştirin!
type: docs
weight: 5000
url: /tr/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

Yazılı erişim sağlar[`FootnoteSeparator`](../footnoteseparator/) bir belgenin düğümleri.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | Birini alır[`FootnoteSeparator`](../footnoteseparator/) belirtilen türde. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## Örnekler

Dipnot ayırıcı formatının nasıl yönetileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Dipnot ayırıcısını hizala.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Ayrıca bakınız

* class [FootnoteSeparator](../footnoteseparator/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
