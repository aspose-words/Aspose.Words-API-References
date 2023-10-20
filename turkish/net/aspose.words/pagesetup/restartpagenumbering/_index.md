---
title: PageSetup.RestartPageNumbering
linktitle: RestartPageNumbering
articleTitle: RestartPageNumbering
second_title: Aspose.Words for .NET
description: PageSetup RestartPageNumbering mülk. Sayfa numaralandırma bölümün başlangıcında yeniden başlıyorsa doğrudur C#'da.
type: docs
weight: 360
url: /tr/net/aspose.words/pagesetup/restartpagenumbering/
---
## PageSetup.RestartPageNumbering property

Sayfa numaralandırma bölümün başlangıcında yeniden başlıyorsa doğrudur.

```csharp
public bool RestartPageNumbering { get; set; }
```

## Notlar

Eğer ayarlanmışsa`YANLIŞ` ,`RestartPageNumbering` özellik the değerini geçersiz kılacak[`PageStartingNumber`](../pagestartingnumber/) sayfa numaralandırmanın önceki bölümden devam edebilmesi için özellik.

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

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
