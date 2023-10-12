---
title: Class ImageSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.ImageSaveOptions sınıf. Belge sayfalarını veya şekilleri görüntülere dönüştürürken ek seçeneklerin belirtilmesine olanak tanır.
type: docs
weight: 5230
url: /tr/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Belge sayfalarını veya şekilleri görüntülere dönüştürürken ek seçeneklerin belirtilmesine olanak tanır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-save-options/) dokümantasyon makalesi.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(SaveFormat) | Oluşturulan görüntüleri the 'ye kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps veyaSvg format. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Kaydedildikten sonra TrueType yazı tiplerini bir belgeye gömerken PostScript ana hatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Renklerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer: **boş dize** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 3B efektlerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | DrawingML şekillerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Ne zaman`doğru` , Aspose.Words'ün adının ve sürümünün üretilen dosyalara yerleştirilmesine neden olur. Varsayılan değer:`doğru` . |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | Görüntü oluşturma modunu ve kalitesini belirlemeye olanak tanır.Graphics nesne. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Oluşturulan görüntülerin yatay çözünürlüğünü inç başına nokta cinsinden alır veya ayarlar. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Oluşturulan görüntülerin parlaklığını alır veya ayarlar. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Oluşturulan görüntüler için renk modunu alır veya ayarlar. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Oluşturulan görüntülerin kontrastını alır veya ayarlar. |
| [ImageSize](../../aspose.words.saving/imagesaveoptions/imagesize/) { get; set; } | Oluşturulan görüntünün boyutunu piksel cinsinden alır veya ayarlar. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Oluşturulan JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun gerçekleştirilip gerçekleştirilmeyeceğini belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer:`YANLIŞ` . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | Oluşturulan çıktıda meta dosyalarının nasıl ele alınacağını belirlemeye izin verir. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Alır veya ayarlar[`NumeralFormat`](../numeralformat/) rakamların oluşturulması için kullanılır. Avrupa rakamları varsayılan olarak kullanılır. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Bayrak, çıktıyı optimize etmenin gerekli olup olmadığını belirtir. Bu bayrak ayarlanırsa, yedekli iç içe tuvaller ve boş tuvaller kaldırılır, ayrıca aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not: Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir: bu özellik şu şekilde ayarlandı:`doğru` . Varsayılan:`YANLIŞ` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Bir belge sabit sayfa formatına aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmenizi sağlar. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | Oluşturulacak sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Oluşturulan görüntüler için arka plan (kağıt) rengini alır veya ayarlar. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Oluşturulan görüntülerin piksel biçimini alır veya ayarlar. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` uygulanabilir olduğu yerde güzel formatlarda çıktı. Varsayılan değer:`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve kaydetme işlemiyle ilgili verileri kabul eder. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Oluşturulan görüntüler için inç başına nokta sayısı cinsinden hem yatay hem de dikey çözünürlüğü ayarlar. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa, oluşturulan belge sayfalarının veya şekillerinin kaydedileceği biçimi belirtir. Raster olabilirTiff ,Png ,Bmp , Jpeg veya vektörEmf ,Eps , Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Oluşturulan görüntüler için yakınlaştırma faktörünü alır veya ayarlar. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Floyd-Steinberg yöntemindeki ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. ne zaman[`ImageBinarizationMethod`](../imagebinarizationmethod/) dır-dirFloydSteinbergDithering . |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Görüntüleri 1 bpp format 'ye dönüştürürken kullanılan yöntemi alır veya ayarlar.[`SaveFormat`](./saveformat/) dır-dirTiff ve [`TiffCompression`](./tiffcompression/) eşittirCcitt3 veyaCcitt4 . |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Oluşturulan görüntüleri TIFF formatında kaydederken uygulanacak sıkıştırma türünü alır veya ayarlar. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer:`YANLIŞ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa formatında kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer:`doğru` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Oluşturma için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | EMF. 'ye kaydederken GDI+ veya Aspose.Words meta dosyası oluşturucusunun kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) oluşturma algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Oluşturulan görüntülerin dikey çözünürlüğünü inç başına nokta cinsinden alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Bu nesnenin derin bir kopyasını oluşturur. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |

### Örnekler

Word belgesinin bir sayfasını şeffaf veya renkli arka plana sahip bir görüntüye dönüştürür.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Şeffaf renk uygulamak için "PaperColor" özelliğini şeffaf renge ayarlayın
// belgeyi bir görüntüye dönüştürürken arka planı.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Bu rengi uygulamak için "PaperColor" özelliğini opak bir renge ayarlayın
// belgeyi bir görüntüye dönüştürdüğümüzde arka plan olarak.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

Bir belgeyi JPEG olarak kaydederken sıkıştırmanın nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Belgeyi oluştururken daha güçlü sıkıştırma kullanmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
// Bu, belgenin dosya boyutunu azaltacaktır ancak görüntü, sıkıştırma kusurlarını daha belirgin bir şekilde görüntüleyecektir.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Belgeyi işlerken daha zayıf sıkıştırma kullanmak için "JpegQuality" özelliğini "100" olarak ayarlayın.
// Bu, dosya boyutunun artması pahasına görüntünün kalitesini artıracaktır.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Bir belgeyi PNG'ye dönüştürürken çözünürlüğün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
            // bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Belgeyi 72dpi çözünürlükte oluşturmak için "Çözünürlük" özelliğini "72" olarak ayarlayın.
            options.Resolution = 72;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // Belgeyi 300dpi çözünürlükte oluşturmak için "Çözünürlük" özelliğini "300" olarak ayarlayın.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


