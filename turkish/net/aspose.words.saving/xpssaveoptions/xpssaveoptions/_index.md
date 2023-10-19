---
title: XpsSaveOptions
linktitle: XpsSaveOptions
articleTitle: XpsSaveOptions
second_title: Aspose.Words for .NET
description: XpsSaveOptions inşaatçı. Bu sınıfın bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Xps format C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Xps format.

```csharp
public XpsSaveOptions()
```

## Örnekler

Kaydedilmiş bir XPS belgesinin ana hatlarında görünecek başlık düzeyinin nasıl sınırlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Seviye 1, 2 ve ardından 3'ün İçindekiler girişi olarak kullanılabilecek başlıklar ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e dönüştürme biçimini değiştirmek için.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Çıktı XPS belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir taslak içerecektir.
// Bu taslaktaki bir girişe tıklamak bizi ilgili başlığın konumuna götürecektir.
// Seviyeleri 2'nin üzerinde olan tüm başlıkları anahattan hariç tutmak için "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayın.
// Yukarıda eklediğimiz son iki başlık görünmeyecek.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ayrıca bakınız

* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## XpsSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Xps veyaOpenXps format.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

## Örnekler

Bir belgenin XPS formatında kitap katlama biçiminde nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e dönüştürme biçimini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// XPS çıktısını kitapçık yapmak için kullanmamıza yardımcı olacak şekilde.
// XPS'yi normal şekilde oluşturmak için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Eğer belgeyi kitapçık olarak işliyorsak "Birden Çok Sayfa" ayarını yapmalıyız
// tüm bölümlerin sayfa kurulum nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak ayarlayın.
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Bu belgeyi yazdırdıktan sonra sayfaları istifleyerek kitapçığa dönüştürebiliriz
// yazıcıdan çıkıp ortadan katlamak için.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
