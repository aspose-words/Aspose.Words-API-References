---
title: "Aspose::Words::Saving::SvgSaveOptions sınıfı"
linktitle: "SvgSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgSaveOptions sınıfı. Bir belgeyi Svg formatında kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 31000
url: /tr/cpp/aspose.words.saving/svgsaveoptions/
---
## SvgSaveOptions class


Bir belgeyi [Svg](../../aspose.words/saveformat/) formatında kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi için [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) belge makalesini ziyaret edin.

```cpp
class SvgSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
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
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Görüntülerin SVG belgesine base64 olarak gömülüp gömülmeyeceğini belirtir. Bu seçeneği etkinleştirmenin, çıktı SVG dosyasının boyutunda önemli bir artışa yol açabileceğini unutmayın. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | **true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur. |
| [get_FitToViewPort](./get_fittoviewport/)() const | Çıktı SVG'sinin kullanılabilir görünüm alanını (tarayıcı penceresini veya kapsayıcıyı) doldurup doldurmayacağını belirtir. **true** olarak ayarlandığında çıktı SVG'nin genişliği ve yüksekliği %100 olarak ayarlanır. Varsayılan değer **false**'dur. |
| [get_IdPrefix](./get_idprefix/)() const | Çıktı belgesindeki tüm oluşturulan öğe kimliklerine (ID) ön ek eklenmesini belirtir. Varsayılan değer null'dır ve hiçbir ön ek eklenmez. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Html belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [get_MaxImageResolution](./get_maximageresolution/)() const | Dışa aktarılan raster görüntülerin çözünürlüğünü sınırlayan inç başına piksel değerini alır veya ayarlar. Varsayılan değer sıfırdır. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri alır. Bu özelliğin varsayılan değeri **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Metafile render seçeneklerini belirtmeye izin verir. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Sayısal render için kullanılan [NumeralFormat](../numeralformat/) değerini alır. Varsayılan olarak Avrupa sayıları kullanılır. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Bayrak, çıktının optimize edilmesinin gerekip gerekmediğini gösterir. Bu bayrak ayarlandığında gereksiz iç içe kanvaslar ve boş kanvaslar kaldırılır, aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not: Bu özellik **true** olarak ayarlanırsa içerik görüntüleme doğruluğu etkilenebilir. Varsayılan **false**'tur. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Render edilecek sayfaları alır veya ayarlar. Varsayılan, belgede bulunan tüm sayfalardır. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | **true** olduğunda, uygulanabilir yerlerde çıktıyı güzel biçimlendirir. Varsayılan değer **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Bir belge kaydedilirken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Bağlantılardan JavaScript'in kaldırılıp kaldırılmayacağını belirtir. Varsayılan **false**'dur. Bu seçenek etkinleştirildiğinde, JavaScript içeren tüm bağlantılar "javascript:void(0)" ile değiştirilir. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Bir belge SVG formatına dışa aktarıldığında kaynakların (görüntülerin) nasıl kaydedileceğini kontrol etmeye olanak tanır. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Bir belge Svg formatına dışa aktarılırken kaynakların (görüntülerin) kaydedildiği fiziksel klasörü belirtir. Varsayılan **null**'dur. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | SVG belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan **null**'dur. |
| [get_SaveFormat](./get_saveformat/)() override | Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. Yalnızca [Svg](../../aspose.words/saveformat/) olabilir. |
| [get_ShowPageBorder](./get_showpageborder/)() const | Sayfanın dış çizgisine bir kenarlık eklenip eklenmeyeceğini kontrol eder. Varsayılan **true**'dur. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_TextOutputMode](./get_textoutputmode/)() const | SVG'de metnin nasıl render edileceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Yazı tipi özniteliklerinin kullanılan karakter koduna göre değiştirilip değiştirilmeyeceğini belirler. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Belgenin sabit sayfa formatına kaydedilmeden önce belirli tipteki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır. Bu özelliğin varsayılan değeri **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | OLE denetimlerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri alır. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Renderleme için anti-aliasing kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Yüksek kalite (yani yavaş) renderleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) için ayarlayıcı. |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Renklerin nasıl işlendiğini belirleyen bir değeri ayarlar. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) için ayarlayıcı. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) için ayarlayıcı. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 3D efektlerin nasıl render edildiğini belirleyen bir değeri ayarlar. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Görüntülerin SVG belgesine base64 olarak gömülüp gömülmeyeceğini belirtir. Bu seçeneği etkinleştirmenin, çıktı SVG dosyasının boyutunda önemli bir artışa yol açabileceğini unutmayın. |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FitToViewPort](./set_fittoviewport/)(bool) | [Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort](./get_fittoviewport/) için ayarlayıcı. |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | [Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix](./get_idprefix/) için ayarlayıcı. |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/) için ayarlayıcı. |
| [set_MaxImageResolution](./set_maximageresolution/)(int32_t) | [Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution](./get_maximageresolution/) için ayarlayıcı. |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **false**'dır. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Metafile render seçeneklerini belirtmeye izin verir. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | [NumeralFormat](../numeralformat/) sayısal karakterlerin işlenmesi için ayarlar. Varsayılan olarak Avrupa rakamları kullanılır. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/) için ayarlayıcı. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/) için ayarlayıcı. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | [Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/) için ayarlayıcı. |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Bir belge SVG formatına dışa aktarıldığında kaynakların (görüntülerin) nasıl kaydedileceğini kontrol etmeye olanak tanır. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | [Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder](./get_resourcesfolder/) için ayarlayıcı. |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | [Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/) için ayarlayıcı. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. Yalnızca [Svg](../../aspose.words/saveformat/) olabilir. |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | [Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder](./get_showpageborder/) için ayarlayıcı. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextOutputMode](./set_textoutputmode/)(Aspose::Words::Saving::SvgTextOutputMode) | [Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode](./get_textoutputmode/) için ayarlayıcı. |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Belirli tipteki alanların, belge sabit sayfa formatına kaydedilmeden önce güncellenip güncellenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **true**'dır. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | OLE kontrollerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri ayarlar. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [SvgSaveOptions](./svgsaveoptions/)() |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
