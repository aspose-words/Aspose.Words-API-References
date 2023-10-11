---
title: Enum ChapterPageSeparator
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ChapterPageSeparator Sıralama. Bölüm ve sayfa numarası arasında görünen ayırıcı karakteri tanımlar.
type: docs
weight: 200
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
| Hyphen | `0` | Bir iki nokta üst üste. |
| Period | `1` | Bir nokta. |
| Colon | `2` | Bir iki nokta üst üste. |
| EmDash | `3` | Vurgulanan bir çizgi. |
| EnDash | `4` | Standart bir çizgi. |

### Örnekler

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


