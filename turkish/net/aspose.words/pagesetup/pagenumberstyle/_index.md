---
title: PageSetup.PageNumberStyle
linktitle: PageNumberStyle
articleTitle: PageNumberStyle
second_title: .NET için Aspose.Words
description: Gelişmiş belge sunumu ve netlik için sayfa numarası biçiminizi kolayca özelleştirmek üzere PageSetup PageNumberStyle özelliğini keşfedin.
type: docs
weight: 320
url: /tr/net/aspose.words/pagesetup/pagenumberstyle/
---
## PageSetup.PageNumberStyle property

Sayfa numarası biçimini alır veya ayarlar.

```csharp
public NumberStyle PageNumberStyle { get; set; }
```

## Örnekler

Bir bölümde sayfa numaralandırmasının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Belge oluşturucuyu ilk bölümün birincil başlığına taşıyın,
// bu bölümdeki her sayfanın görüntüleyeceği.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Mevcut sayfanın numarasını gösterecek bir SAYFA alanı ekleyin.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// SAYFA alanlarının görüntülediği sayfa sayısının 5'ten başlamasını sağlayacak şekilde bölümü yapılandırın.
// Ayrıca, tüm SAYFA alanlarını sayfa numaralarını büyük harfli Roma rakamları kullanarak görüntüleyecek şekilde yapılandırın.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// İkinci bölüm için başka bir SAYFA alanı içeren başka bir birincil başlık oluşturun.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// SAYFA alanlarının görüntülediği sayfa sayısının 10'dan başlaması için bölümü yapılandırın.
// Ayrıca tüm PAGE alanlarını sayfa numaralarını Arap rakamları kullanarak görüntüleyecek şekilde yapılandırın.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Ayrıca bakınız

* enum [NumberStyle](../../numberstyle/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
