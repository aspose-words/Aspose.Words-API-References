---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: .NET için Aspose.Words
description: Belgenizdeki bölüm başlık stillerini daha kolay özelleştirmek ve okunabilirliği ve profesyonelliği artırmak için PageSetup HeadingLevelForChapter özelliğini keşfedin.
type: docs
weight: 180
url: /tr/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Belgedeki bölüm başlıklarına uygulanan başlık düzeyi stilini alır veya ayarlar.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## Notlar

0 ile 9 arasında bir sayı olabilir. 0, sayfa numarasına uygulandığında bölüm numarası olmadığı anlamına gelir.

Bölüm numaralarını içeren sayfa numaraları oluşturabilmeniz için, belge başlıklarına numaralandırılmış bir anahat biçiminin uygulanması gerekir.

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

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
