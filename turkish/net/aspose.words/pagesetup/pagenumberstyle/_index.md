---
title: PageSetup.PageNumberStyle
linktitle: PageNumberStyle
articleTitle: PageNumberStyle
second_title: Aspose.Words for .NET
description: PageSetup PageNumberStyle mülk. Sayfa numarası biçimini alır veya ayarlar C#'da.
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

Bir bölümde sayfa numaralandırmanın nasıl ayarlanacağını gösterir.

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
// o bölümdeki her sayfanın görüntüleneceği.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Geçerli sayfanın numarasını görüntüleyecek bir PAGE alanı ekleyin.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// PAGE alanlarının görüntülediği sayfa sayısının 5'ten başlamasını sağlayacak şekilde bölümü yapılandırın.
// Ayrıca, tüm PAGE alanlarını sayfa numaralarını büyük harf Romen rakamları kullanarak gösterecek şekilde yapılandırın.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// İkinci bölüm için başka bir PAGE alanıyla başka bir birincil başlık oluşturun.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// PAGE alanlarının görüntülediği sayfa sayısının 10'dan başlamasını sağlayacak şekilde bölümü yapılandırın.
// Ayrıca, tüm PAGE alanlarını Arapça sayıları kullanarak sayfa numaralarını gösterecek şekilde yapılandırın.
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
