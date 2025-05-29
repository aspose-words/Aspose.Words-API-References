---
title: PageSetup.PaperSize
linktitle: PaperSize
articleTitle: PaperSize
second_title: .NET için Aspose.Words
description: En iyi yazdırma sonuçlarını elde etmek için belgenizin kağıt boyutunu kolayca özelleştirmek ve yönetmek amacıyla PageSetup PaperSize özelliğini keşfedin.
type: docs
weight: 350
url: /tr/net/aspose.words/pagesetup/papersize/
---
## PageSetup.PaperSize property

Kağıt boyutunu döndürür veya ayarlar.

```csharp
public PaperSize PaperSize { get; set; }
```

## Notlar

Bu özellik güncellemelerini ayarlama[`PageWidth`](../pagewidth/) Ve[`PageHeight`](../pageheight/) değerler. Bu değeri şu şekilde ayarlamakCustom mevcut değerleri değiştirmez.

## Örnekler

JisB4 veya JisB5'in kağıt boyutunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;
// Kağıt boyutunu JisB4 (257x364mm) olarak ayarlayın.
pageSetup.PaperSize = PaperSize.JisB4;
// Alternatif olarak kağıt boyutunu JisB5'e (182x257mm) ayarlayın.
pageSetup.PaperSize = PaperSize.JisB5;
```

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

* enum [PaperSize](../../papersize/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
