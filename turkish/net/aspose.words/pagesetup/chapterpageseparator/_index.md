---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: .NET için Aspose.Words
description: PageSetup'taki ChapterPageSeparator özelliğini keşfedin. Cilalı bir görünüm için bölüm ve sayfa numaraları arasındaki ayırıcı karakteri kolayca özelleştirin.
type: docs
weight: 90
url: /tr/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakteri alır veya ayarlar.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Notlar

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

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
