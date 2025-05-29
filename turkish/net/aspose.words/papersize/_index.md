---
title: PaperSize Enum
linktitle: PaperSize
articleTitle: PaperSize
second_title: .NET için Aspose.Words
description: Belgelerinizde özel kağıt boyutları tanımlamak için Aspose.Words.PaperSize enum'unu keşfedin. Belge biçimlendirmenizi kolaylıkla geliştirin!
type: docs
weight: 5110
url: /tr/net/aspose.words/papersize/
---
## PaperSize enumeration

Kağıt boyutunu belirtir.

```csharp
public enum PaperSize
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| A3 | `0` | 297 x 420 mm. |
| A4 | `1` | 210 x 297 mm. |
| A5 | `2` | 148 x 210 mm. |
| B4 | `3` | 250 x 353 mm. |
| B5 | `4` | 176 x 250 mm. |
| Executive | `5` | 7,25 x 10,5 inç. |
| Folio | `6` | 8,5 x 13 inç. |
| Ledger | `7` | 17 x 11 inç. |
| Legal | `8` | 8,5 x 14 inç. |
| Letter | `9` | 8,5 x 11 inç. |
| EnvelopeDL | `10` | 110x220 mm. |
| Quarto | `11` | 8,47 x 10,83 inç. |
| Statement | `12` | 8,5 x 5,5 inç. |
| Tabloid | `13` | 11 x 17 inç. |
| Paper10x14 | `14` | 10 x 14 inç. |
| Paper11x17 | `15` | 11 x 17 inç. |
| Number10Envelope | `16` | 4,125 x 9,5 inç. |
| JisB4 | `17` | 257 x 364 mm. |
| JisB5 | `18` | 182 x 257 mm. |
| Custom | `19` | Özel kağıt boyutu. |

## Örnekler

Bir bölüm için kağıt boyutunun, yönlendirmenin, kenar boşluklarının ve diğer ayarların nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Sayfa boyutlarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Mevcut sayfanın boyutunu önceden tanımlanmış bir boyuta değiştirebiliriz
// Bu bölümün PageSetup nesnesinin "PaperSize" özelliğini kullanarak.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// Her bölümün kendine ait PageSetup nesnesi vardır. Yeni bir bölüm oluşturmak için bir belge oluşturucu kullandığımızda,
// o bölümün PageSetup nesnesi, önceki bölümün PageSetup nesnesinin tüm değerlerini devralır.
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// Bu bölümün sayfaları için özel bir boyut belirleyin.
builder.PageSetup.PageWidth = 620;
builder.PageSetup.PageHeight = 480;

Assert.AreEqual(PaperSize.Custom, builder.PageSetup.PaperSize);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

doc.Save(ArtifactsDir + "PageSetup.PaperSizes.docx");
```

Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümüyle sonuçlanır.
doc.RemoveAllChildren();

// Bu belgenin artık içerik ekleyebileceğimiz bileşik alt düğümleri yok.
// Düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecektir.
// İlk önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne bir alt bölüm olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa düzeni özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün, tüm içeriklerini barındıracak ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluştur, bazı biçimlendirme özelliklerini ayarla ve sonra onu gövdeye bir alt paragraf olarak ekle.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak, belgeyi yapmak için biraz içerik ekleyin. Bir çalışma oluşturun,
// Görünümünü ve içeriğini ayarlayın ve ardından paragrafın bir alt öğesi olarak ekleyin.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
