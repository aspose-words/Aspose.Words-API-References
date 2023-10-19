---
title: PsSaveOptions Class
linktitle: PsSaveOptions
articleTitle: PsSaveOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PsSaveOptions sınıf. Bir belgeyi bilgisayara kaydederken ek seçenekleri belirlemek için kullanılabilir.Ps format C#'da.
type: docs
weight: 5550
url: /tr/net/aspose.words.saving/pssaveoptions/
---
## PsSaveOptions class

Bir belgeyi bilgisayara kaydederken ek seçenekleri belirlemek için kullanılabilir.Ps format.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-save-options/) dokümantasyon makalesi.

```csharp
public class PsSaveOptions : FixedPageSaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PsSaveOptions](pssaveoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Kaydedildikten sonra TrueType yazı tiplerini bir belgeye gömerken PostScript ana hatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Renklerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer:**boş dize** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words'ün adının ve sürümünün üretilen dosyalara yerleştirilmesine neden olur. Varsayılan değer:`doğru` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Html belgesindeki JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun gerçekleştirilip gerçekleştirilmeyeceğini belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer:`YANLIŞ` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Meta dosyası oluşturma seçeneklerini belirlemeye izin verir. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Alır veya ayarlar[`NumeralFormat`](../numeralformat/) rakamların oluşturulması için kullanılır. Avrupa rakamları varsayılan olarak kullanılır. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Bayrak, çıktıyı optimize etmenin gerekli olup olmadığını belirtir. Bu bayrak ayarlanırsa, yedekli iç içe tuvaller ve boş tuvaller kaldırılır, ayrıca aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not: Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir: bu özellik şu şekilde ayarlandı:`doğru` . Varsayılan:`YANLIŞ` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Bir belge sabit sayfa formatına aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Oluşturulacak sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` uygulanabilir olduğu yerde güzel formatlarda çıktı. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve kaydetme işlemiyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/pssaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaPs . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer:`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa formatında kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer:`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Oluşturma için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/) { get; set; } | Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir boole değeri alır veya ayarlar, ile belirtilirse[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) oluşturma algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |

## Örnekler

Bir belgenin Postscript formatında kitap katlama biçiminde nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi PostScript'e dönüştürme biçimini değiştirmek için.
// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// çıktı Postscript belgesinde, bundan bir kitapçık oluşturmamıza yardımcı olacak şekilde.
// Belgeyi normal şekilde kaydetmek için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Eğer belgeyi kitapçık olarak işliyorsak "Birden Çok Sayfa" ayarını yapmalıyız
// tüm bölümlerin sayfa kurulum nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak ayarlayın.
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Bu belgeyi sayfaların her iki tarafına da yazdırdıktan sonra tüm sayfaları aynı anda ortadan katlayabiliriz,
// ve içerikler kitapçık oluşturacak şekilde sıralanacaktır.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
