---
title: ImageSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: Belge sayfalarını veya şekilleri görüntülere dönüştürürken ek seçenekleri belirlemeye izin verir.
type: docs
weight: 4970
url: /tr/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Belge sayfalarını veya şekilleri görüntülere dönüştürürken ek seçenekleri belirlemeye izin verir.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(SaveFormat) | İşlenen görüntüleri the içine kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatırTiff ,Png ,Bmp , Emf ,Jpeg veyaSvg biçim. Png ,Bmp ,Jpeg veyaSvg biçim. |

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
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | için işleme modunu ve kalitesini belirlemeye izin verir.Graphics nesne. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Oluşturulan görüntülerin yatay çözünürlüğünü inç başına nokta olarak alır veya ayarlar. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Oluşturulan görüntülerin parlaklığını alır veya ayarlar. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Oluşturulan görüntüler için renk modunu alır veya ayarlar. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Oluşturulan görüntülerin kontrastını alır veya ayarlar. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar. |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Oluşturulan JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | İşlenen çıktıda meta dosyaların nasıl ele alınacağını belirlemeye izin verir. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Alır veya ayarlar[`NumeralFormat`](../numeralformat/) sayıların işlenmesi için kullanılır. Varsayılan olarak Avrupa rakamları kullanılır. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Bayrak, çıktının optimize edilmesinin gerekip gerekmediğini gösterir. Bu bayrak ayarlanırsa, fazladan iç içe tuvaller ve boş tuvaller kaldırılırsa, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir: bu özellik true olarak ayarlanmıştır. Varsayılan değer false'tur. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Bir belge sabit sayfa formatına aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | Oluşturulacak sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Oluşturulan görüntüler için arka plan (kağıt) rengini alır veya ayarlar. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Oluşturulan görüntüler için piksel biçimini alır veya ayarlar. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Ne zaman`doğru` , uygun olduğunda güzel biçimler çıktısı. Varsayılan değer **yanlış** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Bir belge kaydedilirken çağrılır ve ilerleme kaydetmeyle ilgili verileri kabul eder. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Oluşturulan görüntüler için nokta/inç olarak hem yatay hem de dikey çözünürlüğü ayarlar. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Bu kaydetme seçenekleri nesnesi kullanılırsa, oluşturulan belge sayfalarının veya şekillerinin kaydedileceği biçimi belirtir. Bir raster olabilirTiff ,Png ,Bmp , Jpeg veya vektörEmf ,Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Oluşturulan görüntüler için yakınlaştırma faktörünü alır veya ayarlar. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Floyd-Steinberg yöntemindeki ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. [`ImageBinarizationMethod`](../imagebinarizationmethod/) ImageBinarizationMethod.FloydSteinbergDithering. 'dir |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Görüntüleri 1 bpp formatına dönüştürürken kullanılan yöntemi alır veya ayarlar [`SaveFormat`](./saveformat/) SaveFormat.Tiff ve 'dir[`TiffCompression`](./tiffcompression/) TiffCompression.Ccitt3 veya TiffCompression.Ccitt4. 'ye eşittir |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Oluşturulan görüntüleri TIFF biçiminde kaydederken uygulanacak sıkıştırma türünü alır veya ayarlar. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türlerdeki alanların güncellenmesi gerekip gerekmediğini belirleyen bir değer alır veya ayarlar. Bu özellik için varsayılan değer **doğru** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | olup olmadığını belirleyen bir değer alır veya ayarlar.[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | İçeriğin olup olmadığını belirleyen değeri alır veya ayarlar.[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) kaydetmeden önce güncellenir. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | EMF'ye kaydederken GDI+ veya Aspose.Words meta dosyası oluşturucu kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Oluşturulan görüntülerin dikey çözünürlüğünü inç başına nokta olarak alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Bu nesnenin derin bir klonunu oluşturur. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |

### Örnekler

Bir Word belgesinin bir sayfasını saydam veya renkli arka plana sahip bir görüntüye dönüştürür.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Saydam bir renk uygulamak için "PaperColor" özelliğini saydam bir renge ayarlayın
// bir görüntüye dönüştürülürken belgenin arka planı.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// "PaperColor" özelliğini o rengi uygulamak için opak bir renge ayarlayın
// bir görüntüye dönüştürürken belgenin arka planı olarak.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

Bir belgeyi JPEG olarak kaydederken sıkıştırmanın nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Belgeyi oluştururken daha güçlü sıkıştırma kullanmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
// Bu, belgenin dosya boyutunu küçültecek, ancak görüntü daha belirgin sıkıştırma yapaylıkları gösterecektir.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Belgeyi işlerken daha zayıf sıkıştırma kullanmak için "JpegQuality" özelliğini "100" olarak ayarlayın.
// Bu, artan dosya boyutu pahasına görüntünün kalitesini artıracaktır.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Bir belgeyi PNG'ye dönüştürürken çözünürlüğün nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
            // bu yöntemin belgeyi bir görüntüye dönüştürme şeklini değiştirmek için.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Belgeyi 72dpi'de işlemek için "Resolution" özelliğini "72" olarak ayarlayın.
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
            // Belgeyi 300 dpi'de işlemek için "Çözünürlük" özelliğini "300" olarak ayarlayın.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
