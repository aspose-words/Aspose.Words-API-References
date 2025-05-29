---
title: ImageSaveOptions Class
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.ImageSaveOptions'ı keşfedin. Yüksek kaliteli görüntü çıktısı için özelleştirilebilir seçeneklerle belgenizi kolayca işleyin.
type: docs
weight: 5980
url: /tr/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Belge sayfalarını veya şekillerini resimlere dönüştürürken ek seçeneklerin belirtilmesine olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-save-options/) belgeleme makalesi.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Bu sınıfın, işlenmiş görüntüleri içinde kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps , WebP veyaSvg biçim. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Renklerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` . |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | İşleme modunu ve kalitesini belirtmenize olanak tanırGraphics nesne. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Oluşturulan görüntülerin yatay çözünürlüğünü inç başına nokta cinsinden alır veya ayarlar. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Oluşturulan görüntülerin parlaklığını alır veya ayarlar. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Oluşturulan görüntüler için renk modunu alır veya ayarlar. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Oluşturulan görüntülerin kontrastını alır veya ayarlar. |
| [ImageSize](../../aspose.words.saving/imagesaveoptions/imagesize/) { get; set; } | Oluşturulan bir görüntünün boyutunu piksel cinsinden alır veya ayarlar. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar. |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Oluşturulan JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | Meta dosyalarının işlenen çıktıda nasıl işleneceğini belirtmeye izin verir. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Alır veya ayarlar[`NumeralFormat`](../numeralformat/) rakamların işlenmesi için kullanılır. Varsayılan olarak Avrupa rakamları kullanılır. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Bayrağı, çıktının optimize edilmesinin gerekip gerekmediğini belirtir. Bu bayrak ayarlanırsa, gereksiz iç içe geçmiş tuvaller ve boş tuvaller kaldırılır, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Bu özellik olarak ayarlanırsa içerik görüntüsünün doğruluğu etkilenebilir.`doğru` . Varsayılan`YANLIŞ` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Bir belge sabit sayfa biçimine aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | İşlenecek sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Oluşturulan resimler için arka plan (kağıt) rengini alır veya ayarlar. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Oluşturulan görüntülerin piksel biçimini alır veya ayarlar. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belgeyi kaydederken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Oluşturulan görüntüler için hem yatay hem de dikey çözünürlüğü inç başına nokta cinsinden ayarlar. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa, işlenen belge sayfalarının veya şekillerinin kaydedileceği biçimi belirtir. Bir raster olabilir Tiff ,Png ,Bmp , Jpeg veya vektörEmf ,Eps , WebP ,Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Oluşturulan görüntüler için yakınlaştırma faktörünü alır veya ayarlar. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Floyd-Steinberg yöntemindeki ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. ne zaman[`ImageBinarizationMethod`](../imagebinarizationmethod/) dırFloydSteinbergDithering . |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Görüntüleri 1 bpp formatına dönüştürürken kullanılan yöntemi alır veya ayarlar [`SaveFormat`](./saveformat/) dırTiff ve [`TiffCompression`](./tiffcompression/) eşittirCcitt3 veyaCcitt4 . |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Oluşturulan görüntüleri TIFF biçimine kaydederken uygulanacak sıkıştırma türünü alır veya ayarlar. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Kullanılan karakter koduna göre yazı tipi özniteliklerinin değiştirilip değiştirilmeyeceğini belirler. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türdeki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değeri alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | EMF'ye kaydederken GDI+ veya Aspose.Words meta dosyası oluşturucusunun kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Oluşturulan görüntülerin dikey çözünürlüğünü inç başına nokta cinsinden alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Bu nesnenin derin bir klonunu oluşturur. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |

## Örnekler

Bir belgeyi PNG'ye dönüştürürken çözünürlüğün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Belgeyi 72 dpi olarak görüntülemek için "Çözünürlük" özelliğini "72" olarak ayarlayın.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Belgeyi 300 dpi olarak işlemek için "Çözünürlük" özelliğini "300" olarak ayarlayın.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

Bir belgeyi JPEG olarak kaydederken sıkıştırmanın nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Belgeyi işlerken daha güçlü sıkıştırma kullanmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
// Bu, belgenin dosya boyutunu küçültecektir, ancak görüntü daha belirgin sıkıştırma eserleri gösterecektir.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Belgeyi işlerken daha zayıf sıkıştırma kullanmak için "JpegQuality" özelliğini "100" olarak ayarlayın.
// Bu, dosya boyutunun artması pahasına görüntünün kalitesini artıracaktır.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

Word belgesinin bir sayfasını şeffaf veya renkli arka planlı bir görüntüye dönüştürür.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// Şeffaf bir renk uygulamak için "PaperColor" özelliğini şeffaf bir renge ayarlayın
// belgenin görüntüye dönüştürülmesi sırasında arka plan olarak kullanılır.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Bu rengi uygulamak için "PaperColor" özelliğini opak bir renge ayarlayın
// belgeyi bir görüntüye dönüştürdüğümüzde arka plan olarak kullanırız.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
