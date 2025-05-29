---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi ve netlik için bölüm ve sayfa numarası ayırıcılarını özelleştirmek üzere Aspose.Words.ChapterPageSeparator numaralandırmasını keşfedin.
type: docs
weight: 390
url: /tr/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Bölüm ve sayfa numarası arasında görünen ayırıcı karakteri tanımlar.

```csharp
public enum ChapterPageSeparator
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Hyphen | `0` | İki nokta üst üste. |
| Period | `1` | Bir dönem. |
| Colon | `2` | İki nokta üst üste. |
| EmDash | `3` | Vurgulanmış bir çizgi. |
| EnDash | `4` | Standart bir çizgi. |

## Örnekler

Sayfa bölümleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Ayrıca bakınız

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
