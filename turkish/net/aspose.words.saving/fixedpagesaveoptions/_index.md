---
title: Class FixedPageSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.FixedPageSaveOptions sınıf. Bir belgeyi sabit sayfa biçimlerine PDF XPS resimler vb. kaydederken belirtilebilecek genel seçenekleri içerir.
type: docs
weight: 4760
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/
---
## FixedPageSaveOptions class

Bir belgeyi sabit sayfa biçimlerine (PDF, XPS, resimler vb.) kaydederken belirtilebilecek genel seçenekleri içerir.

```csharp
public abstract class FixedPageSaveOptions : SaveOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | TrueType yazı tiplerini bir belgeye gömerken PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer şudur: **yanlış** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Renklerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer **boş dize** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Doğru olduğunda, Aspose.Words'ün adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değerdir **doğru** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Html belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Meta dosyası oluşturma seçeneklerini belirlemeye izin verir. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Alır veya ayarlar[`NumeralFormat`](../numeralformat/) sayıların işlenmesi için kullanılır. Varsayılan olarak Avrupa rakamları kullanılır. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Bayrak, çıktının optimize edilmesinin gerekip gerekmediğini gösterir. Bu bayrak ayarlanırsa, fazladan iç içe tuvaller ve boş tuvaller kaldırılırsa, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir: bu özellik true olarak ayarlanmıştır. Varsayılan değer false'tur. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Bir belge sabit sayfa formatına aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Oluşturulacak sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğunda güzel biçimler çıktısı. Varsayılan değer **yanlış** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve ilerleme kaydetmeyle ilgili verileri kabul eder. |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği formatı belirtir. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer **doğru** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | İçeriğin olup olmadığını belirleyen değeri alır veya ayarlar.[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) kaydetmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |

### Örnekler

Bir belgenin her sayfasının ayrı bir TIFF görüntüsüne nasıl işleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // "PageSet" özelliğini ilk sayfanın numarasına ayarlayın
    // belgeyi oluşturmaya başlamak için.
    options.PageSet = new PageSet(i);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Bir belgeden bir sayfanın bir JPEG görüntüsüne nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// aracılığıyla ikinci sayfayı seçmek için "PageSet"i "1" olarak ayarlayın.
// belgeyi oluşturmaya başlamak için sıfır tabanlı dizin.
options.PageSet = new PageSet(1);

// Belgeyi JPEG formatında kaydettiğimizde Aspose.Words sadece bir sayfa oluşturuyor.
// Bu resim ikinci sayfadan başlayarak bir sayfa içerecek,
// orijinal belgenin sadece ikinci sayfası olacak.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Ayrıca bakınız

* class [SaveOptions](../saveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


