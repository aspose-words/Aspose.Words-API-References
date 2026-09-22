---
title: "Aspose::Words::Saving::ImageSaveOptions class"
linktitle: "ImageSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions sınıfı. Belge sayfalarını veya şekilleri görüntülere render ederken ek seçenekler belirtmeye olanak tanır. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class


Belge sayfalarını veya şekilleri görüntülere render ederken ek seçenekleri belirtmeye izin verir. Daha fazla bilgi için, [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) dokümantasyon makalesini ziyaret edin.

```cpp
class ImageSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | Bu nesnenin derin bir klonunu oluşturur. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Belirtilen kaydetme formatı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Verilen dosya adında belirtilen dosya uzantısı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Bir belge kaydedildiğinde TrueType yazı tiplerini gömerek PostScript konturlarıyla yazı tiplerinin gömülmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Renklerin nasıl render edildiğini belirleyen bir değeri alır. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Varsayılan şablona (dosya adı dahil) yolu alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**'dir. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 3D efektlerinin nasıl işleneceğini belirleyen bir değeri alır. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | **true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur. |
| [get_GraphicsQualityOptions](./get_graphicsqualityoptions/)() const | **Graphics** nesnesi için renderleme modunu ve kalitesini belirtmeye olanak tanır. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Oluşturulan görüntüler için yatay çözünürlüğü alır veya ayarlar, inç başına nokta (dpi) cinsinden. |
| [get_ImageBrightness](./get_imagebrightness/)() const | Oluşturulan görüntüler için parlaklığı alır veya ayarlar. |
| [get_ImageColorMode](./get_imagecolormode/)() const | Oluşturulan görüntüler için renk modunu alır veya ayarlar. |
| [get_ImageContrast](./get_imagecontrast/)() const | Oluşturulan görüntüler için kontrastı alır veya ayarlar. |
| [get_ImageSize](./get_imagesize/)() const | Oluşturulan bir görüntünün boyutunu piksel cinsinden alır veya ayarlar. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar. |
| [get_JpegQuality](./get_jpegquality/)() | Oluşturulan JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Html belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri alır. Bu özelliğin varsayılan değeri **false**. |
| [get_MetafileRenderingOptions](./get_metafilerenderingoptions/)() | Renderlenen çıktıda metafillerin nasıl işlendiğini belirtmeye olanak tanır. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Metafile render seçeneklerini belirtmeye izin verir. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Sayısal render için kullanılan [NumeralFormat](../numeralformat/) değerini alır. Varsayılan olarak Avrupa sayıları kullanılır. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Bayrak, çıktının optimize edilmesinin gerekip gerekmediğini gösterir. Bu bayrak ayarlandığında gereksiz iç içe kanvaslar ve boş kanvaslar kaldırılır, aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not: Bu özellik **true** olarak ayarlanırsa içerik görüntüleme doğruluğu etkilenebilir. Varsayılan **false**'tur. |
| [get_PageLayout](./get_pagelayout/)() const | Birden fazla sayfayı tek bir çıktıya render ederken kullanılan düzeni alır veya ayarlar. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [get_PageSet](./get_pageset/)() | Render edilecek sayfaları alır veya ayarlar. Varsayılan, belgede bulunan tüm sayfalardır. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Render edilecek sayfaları alır veya ayarlar. Varsayılan, belgede bulunan tüm sayfalardır. |
| [get_PaperColor](./get_papercolor/)() | Oluşturulan görüntüler için arka plan (kağıt) rengini alır veya ayarlar. Varsayılan değer **White**'dır. |
| [get_PixelFormat](./get_pixelformat/)() const | Oluşturulan görüntüler için piksel formatını alır veya ayarlar. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | **true** olduğunda, uygulanabilir yerlerde çıktıyı güzel biçimlendirir. Varsayılan değer **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Bir belge kaydedilirken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [get_SaveFormat](./get_saveformat/)() override | Bu kaydetme seçenekleri nesnesi kullanılırsa renderlenen belge sayfalarının veya şekillerin kaydedileceği formatı belirtir. Raster bir [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/) ya da vektör bir [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../), [Svg](../../aspose.words/saveformat/) olabilir. |
| [get_Scale](./get_scale/)() const | Oluşturulan görüntüler için yakınlaştırma faktörünü alır veya ayarlar. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/)() const | Floyd-Steinberg yönteminde ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. [ImageBinarizationMethod](../imagebinarizationmethod/) [FloydSteinbergDithering](../imagebinarizationmethod/) olduğunda. |
| [get_TiffBinarizationMethod](./get_tiffbinarizationmethod/)() const | Görüntüleri 1 bpp formatına dönüştürürken kullanılan yöntemi alır veya ayarlar; [SaveFormat](./get_saveformat/) [Tiff](../../aspose.words/saveformat/) ve [TiffCompression](./get_tiffcompression/) [Ccitt3](../tiffcompression/) veya [Ccitt4](../tiffcompression/) olduğunda. |
| [get_TiffCompression](./get_tiffcompression/)() const | Oluşturulan görüntüleri TIFF formatında kaydederken uygulanacak sıkıştırma türünü alır veya ayarlar. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Yazı tipi özniteliklerinin kullanılan karakter koduna göre değiştirilip değiştirilmeyeceğini belirler. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Belgenin sabit sayfa formatına kaydedilmeden önce belirli tipteki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır. Bu özelliğin varsayılan değeri **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | OLE denetimlerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri alır. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Renderleme için anti-aliasing kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseGdiEmfRenderer](./get_usegdiemfrenderer/)() const | EMF olarak kaydederken GDI+ veya Aspose.Words metafile renderleyicisinin kullanılacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Yüksek kalite (yani yavaş) renderleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Oluşturulan görüntüler için dikey çözünürlüğü, inç başına nokta (dpi) cinsinden alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [ImageSaveOptions](./imagesaveoptions/)(Aspose::Words::SaveFormat) | Bu sınıfın, renderlanan görüntüleri [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/), [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../) veya [Svg](../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilecek yeni bir örneğini başlatır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) için ayarlayıcı. |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Renklerin nasıl işlendiğini belirleyen bir değeri ayarlar. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) için ayarlayıcı. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) için ayarlayıcı. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 3D efektlerin nasıl render edildiğini belirleyen bir değeri ayarlar. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_GraphicsQualityOptions](./set_graphicsqualityoptions/)(const System::SharedPtr\<Aspose::Words::Saving::GraphicsQualityOptions\>\&) | [Aspose::Words::Saving::ImageSaveOptions::get_GraphicsQualityOptions](./get_graphicsqualityoptions/) için ayarlayıcı. |
| [set_HorizontalResolution](./set_horizontalresolution/)(float) | [Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution](./get_horizontalresolution/) için ayarlayıcı. |
| [set_ImageBrightness](./set_imagebrightness/)(float) | [Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness](./get_imagebrightness/) için ayarlayıcı. |
| [set_ImageColorMode](./set_imagecolormode/)(Aspose::Words::Saving::ImageColorMode) | [Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode](./get_imagecolormode/) için ayarlayıcı. |
| [set_ImageContrast](./set_imagecontrast/)(float) | [Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast](./get_imagecontrast/) için ayarlayıcı. |
| [set_ImageSize](./set_imagesize/)(System::Drawing::Size) | [Aspose::Words::Saving::ImageSaveOptions::get_ImageSize](./get_imagesize/) için ayarlayıcı. |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | [Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality](./get_jpegquality/) için ayarlayıcı. |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **false**'dır. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Metafile render seçeneklerini belirtmeye izin verir. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | [NumeralFormat](../numeralformat/) sayısal karakterlerin işlenmesi için ayarlar. Varsayılan olarak Avrupa rakamları kullanılır. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/) için ayarlayıcı. |
| [set_PageLayout](./set_pagelayout/)(const System::SharedPtr\<Aspose::Words::Saving::MultiPageLayout\>\&) | [Aspose::Words::Saving::ImageSaveOptions::get_PageLayout](./get_pagelayout/) için ayarlayıcı. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [set_PageSet](./set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | [Aspose::Words::Saving::ImageSaveOptions::get_PageSet](./get_pageset/) için ayarlayıcı. |
| [set_PaperColor](./set_papercolor/)(System::Drawing::Color) | [Aspose::Words::Saving::ImageSaveOptions::get_PaperColor](./get_papercolor/) için ayarlayıcı. |
| [set_PixelFormat](./set_pixelformat/)(Aspose::Words::Saving::ImagePixelFormat) | [Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat](./get_pixelformat/) için ayarlayıcı. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_Resolution](./set_resolution/)(float) | Oluşturulan görüntüler için hem yatay hem de dikey çözünürlüğü, inç başına nokta (dpi) cinsinden ayarlar. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | [Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat](./get_saveformat/) için ayarlayıcı. |
| [set_Scale](./set_scale/)(float) | [Aspose::Words::Saving::ImageSaveOptions::get_Scale](./get_scale/) için ayarlayıcı. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_ThresholdForFloydSteinbergDithering](./set_thresholdforfloydsteinbergdithering/)(uint8_t) | [Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/) için ayarlayıcı. |
| [set_TiffBinarizationMethod](./set_tiffbinarizationmethod/)(Aspose::Words::Saving::ImageBinarizationMethod) | [Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod](./get_tiffbinarizationmethod/) için ayarlayıcı. |
| [set_TiffCompression](./set_tiffcompression/)(Aspose::Words::Saving::TiffCompression) | [Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression](./get_tiffcompression/) için ayarlayıcı. |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Belirli tipteki alanların, belge sabit sayfa formatına kaydedilmeden önce güncellenip güncellenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **true**'dır. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | OLE kontrollerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri ayarlar. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseGdiEmfRenderer](./set_usegdiemfrenderer/)(bool) | [Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer](./get_usegdiemfrenderer/) için ayarlayıcı. |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_VerticalResolution](./set_verticalresolution/)(float) | [Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution](./get_verticalresolution/) için ayarlayıcı. |
| static [Type](./type/)() |  |

## Örnekler



Bir Word belgesinin sayfasını şeffaf veya renkli arka planlı bir görüntüye renderlar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Şeffaf bir renk uygulamak için \"PaperColor\" özelliğini şeffaf bir renge ayarlayın
// belgeyi bir görüntüye render ederken belgeye arka plan ekleyin.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// \"PaperColor\" özelliğini opak bir renge ayarlayarak o rengi uygulayın
// belgeyi bir görüntüye render ederken belgeye arka plan olarak
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```


Bir belgeyi JPEG olarak kaydederken sıkıştırmayı nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// \"JpegQuality\" özelliğini \"10\" olarak ayarlayarak belgeyi render ederken daha güçlü sıkıştırma kullanın.
// Bu, belgenin dosya boyutunu azaltacak, ancak görüntü daha belirgin sıkıştırma artefaktları gösterecektir.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// \"JpegQuality\" özelliğini \"100\" olarak ayarlayarak belgeyi render ederken daha zayıf sıkıştırma kullanın.
// Bu, dosya boyutunun artması pahasına görüntü kalitesini artıracaktır.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```


Bir belgeyi PNG'ye render ederken çözünürlüğü nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// \"Resolution\" özelliğini \"72\" olarak ayarlayarak belgeyi 72dpi'de render edin.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// \"Resolution\" özelliğini \"300\" olarak ayarlayarak belgeyi 300dpi'de render edin.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## Ayrıca Bakınız

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
