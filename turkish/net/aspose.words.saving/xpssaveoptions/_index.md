---
title: XpsSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Bir belgeyi dosyaya kaydederken ek seçenekleri belirtmek için kullanılabilir.Xps biçim.
type: docs
weight: 5430
url: /tr/net/aspose.words.saving/xpssaveoptions/
---
## XpsSaveOptions class

Bir belgeyi dosyaya kaydederken ek seçenekleri belirtmek için kullanılabilir.Xps biçim.

```csharp
public class XpsSaveOptions : FixedPageSaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [XpsSaveOptions](xpssaveoptions/#constructor)() | Bu sınıfın, bir document dosyasını şuraya kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Xps biçim. |
| [XpsSaveOptions](xpssaveoptions/#constructor_1)(SaveFormat) | Bu sınıfın, bir document dosyasını şuraya kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Xps veyaOpenXps biçim. |

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
| [OutlineOptions](../../aspose.words.saving/xpssaveoptions/outlineoptions/) { get; } | Anahat seçeneklerini belirlemeye izin verir. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Bir belge sabit sayfa formatına aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Oluşturulacak sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğunda güzel biçimler çıktısı. Varsayılan değer **yanlış** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve ilerleme kaydetmeyle ilgili verileri kabul eder. |
| override [SaveFormat](../../aspose.words.saving/xpssaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaXps . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer **doğru** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | İçeriğin olup olmadığını belirleyen değeri alır veya ayarlar.[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) kaydetmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/) { get; set; } | Belgenin bir kitapçık yazdırma düzeni kullanılarak kaydedilmesi gerekip gerekmediğini belirten bir boole değeri alır veya ayarlar, aracılığıyla belirtilirse[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |

### Örnekler

Kaydedilmiş bir XPS belgesinin ana hatlarında görünecek başlıkların düzeyinin nasıl sınırlandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Seviye 1, 2 ve ardından 3 TOC girişleri olarak hizmet edebilecek başlıklar ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'ye dönüştürme şeklini değiştirmek için.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Çıktı XPS belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir anahat içerecektir.
// Bu taslakta bir girdiye tıklamak bizi ilgili başlığın konumuna götürecektir.
// Seviyeleri 2'nin üzerinde olan tüm başlıkları anahattan çıkarmak için "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayın.
// Yukarıda eklediğimiz son iki başlık görünmeyecektir.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
