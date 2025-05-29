---
title: XpsSaveOptions
linktitle: XpsSaveOptions
articleTitle: XpsSaveOptions
second_title: .NET için Aspose.Words
description: Belgelerinizi XPS formatında kaydetmek için örnekleri zahmetsizce oluşturmak ve belge yönetimi verimliliğinizi artırmak için XpsSaveOptions oluşturucusunu keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Xps biçim.

```csharp
public XpsSaveOptions()
```

## Örnekler

Kaydedilmiş bir XPS belgesinin ana hatlarında görünecek başlıkların düzeyinin nasıl sınırlandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 1, 2 ve sonra 3. düzeylerde İçindekiler girişi olarak kullanılabilecek başlıklar ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e nasıl dönüştüreceğini değiştirmek için.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Çıktı XPS belgesi, belge gövdesindeki başlıkları listeleyen bir içerik tablosu olan bir ana hat içerecektir.
// Bu taslaktaki bir girdiye tıkladığımızda ilgili başlığın bulunduğu yere gideceğiz.
// Anahattan 2'nin üstündeki tüm başlıkları hariç tutmak için "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayın.
// Yukarıda eklediğimiz son iki başlık görünmeyecektir.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ayrıca bakınız

* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## XpsSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Xps veyaOpenXps biçim.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

## Örnekler

Bir belgenin kitap katlaması şeklinde XPS formatına nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e nasıl dönüştüreceğini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// çıktıda XPS'i kitapçık yapmak için kullanmamıza yardımcı olacak şekilde.
// XPS'i normal şekilde işlemek için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Belgeyi kitapçık olarak oluşturuyorsak, "Çoklu Sayfalar"ı ayarlamalıyız
// tüm bölümlerin sayfa kurulumu nesnelerinin özellikleri "MultiplePagesType.BookFoldPrinting" olarak değiştirildi.
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Bu belgeyi yazdırdığımızda, sayfaları üst üste koyarak bir kitapçığa dönüştürebiliriz
// yazıcıdan çıkıp ortadan katlanmak.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
