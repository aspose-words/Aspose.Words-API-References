---
title: PageSetup.HeadingLevelForChapter
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Belgedeki bölüm başlıklarına uygulanan başlık düzeyi stilini alır veya ayarlar.
type: docs
weight: 180
url: /tr/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Belgedeki bölüm başlıklarına uygulanan başlık düzeyi stilini alır veya ayarlar.

```csharp
public int HeadingLevelForChapter { get; set; }
```

### Notlar

0'dan 9'a kadar bir sayı olabilir. 0, sayfa numarasına uygulandığında bölüm numarası olmadığı anlamına gelir.

Bölüm numaralarını içeren sayfa numaralarını oluşturabilmeniz için, belge başlıklarına numaralı anahat biçiminin uygulanması gerekir.

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

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


