---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions sınıfı"
linktitle: "HtmlFixedSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions sınıfı. Bir belgeyi HtmlFixed biçimine kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


Bir belgeyi [HtmlFixed](../../aspose.words/saveformat/) biçimine kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi edinmek için [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) belge makalesini ziyaret edin.

```cpp
class HtmlFixedSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Belirtilen kaydetme formatı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Verilen dosya adında belirtilen dosya uzantısı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Bir belge kaydedildiğinde TrueType yazı tiplerini gömerek PostScript konturlarıyla yazı tiplerinin gömülmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Renklerin nasıl render edildiğini belirleyen bir değeri alır. |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | style.css dosyasındaki tüm sınıf adlarına eklenen önek belirtir. Varsayılan değer **%\"aw\"**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Varsayılan şablona (dosya adı dahil) yolu alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**'dir. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 3D efektlerinin nasıl işleneceğini belirleyen bir değeri alır. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_Encoding](./get_encoding/)() const | HTML'ye dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer **new UTF8Encoding(true)** (BOM'lu UTF-8). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | CSS'in (Kademeli [Style](../../aspose.words/style/) Sayfası) HTML belgesine gömülüp gömülmeyeceğini belirtir. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | Yazı tiplerinin HTML belgesine Base64 biçiminde gömülüp gömülmeyeceğini belirtir. Bu bayrağın ayarlanmasının çıktı HTML dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Görsellerin HTML belgesine Base64 biçiminde gömülüp gömülmeyeceğini belirtir. Bu bayrağın ayarlanmasının çıktı HTML dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | SVG kaynaklarının HTML belgesine gömülüp gömülmeyeceğini belirtir. Varsayılan değer **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | Form alanlarının metin veya grafik olarak dönüştürülmek yerine etkileşimli öğeler ('input' etiketi) olarak dışa aktarılıp aktarılmayacağını alır veya ayarlar. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | **true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur. |
| [get_FontFormat](./get_fontformat/)() const | Yazı tipi dışa aktarma için kullanılan [ExportFontFormat](../exportfontformat/) alır veya ayarlar. Varsayılan değer [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | Çıktı belgesindeki tüm oluşturulan öğe kimliklerine (ID) ön ek eklenmesini belirtir. Varsayılan değer null'dır ve hiçbir ön ek eklenmez. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Html belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri alır. Bu özelliğin varsayılan değeri **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Metafile render seçeneklerini belirtmeye izin verir. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Sayısal render için kullanılan [NumeralFormat](../numeralformat/) değerini alır. Varsayılan olarak Avrupa sayıları kullanılır. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | Çıktının optimize edilmesinin gerekip gerekmediğini gösteren bayrak. Bu bayrak ayarlandığında gereksiz iç içe kanvaslar ve boş kanvaslar kaldırılır, aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not: Bu özellik **true** olarak ayarlandığında içeriğin görüntülenme doğruluğu etkilenebilir. Varsayılan **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | HTML belgesindeki sayfaların yatay hizalamasını belirtir. Varsayılan değer [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | HTML belgesindeki sayfaların etrafındaki kenar boşluklarını belirtir. Kenar boşluğu değeri puan cinsinden ölçülür ve 0'a eşit ya da daha büyük olmalıdır. Varsayılan değer 10 puandır. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Render edilecek sayfaları alır veya ayarlar. Varsayılan, belgede bulunan tüm sayfalardır. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | **true** olduğunda, uygulanabilir yerlerde çıktıyı güzel biçimlendirir. Varsayılan değer **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Bir belge kaydedilirken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Bağlantılardan JavaScript'in kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Bir belge sabit sayfa HTML formatına dışa aktarıldığında kaynakların (görseller, yazı tipleri ve css) nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Bir belge HTML formatına dışa aktarılırken kaynakların (görseller, yazı tipleri, css) kaydedileceği fiziksel klasörü belirtir. Varsayılan **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasör adını belirtir. Varsayılan **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | Bir belge harici stil sayfası ile kaydedildiğinde (yani [ExportEmbeddedCss](./get_exportembeddedcss/) **false** olduğunda) \"@font-face\" CSS kurallarının ayrı bir dosya \"fontFaces.css\" içine konulup konulmayacağını gösteren bayrak. Varsayılan değer **false**, tüm CSS kuralları tek dosya \"styles.css\" içine yazılır. |
| [get_SaveFormat](./get_saveformat/)() override | Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği biçimi belirtir. Sadece [HtmlFixed](../../aspose.words/saveformat/) olabilir. |
| [get_ShowPageBorder](./get_showpageborder/)() const | Sayfaların etrafındaki kenarlığın gösterilip gösterilmeyeceğini belirtir. Varsayılan **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Yazı tipi özniteliklerinin kullanılan karakter koduna göre değiştirilip değiştirilmeyeceğini belirler. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Belgenin sabit sayfa formatına kaydedilmeden önce belirli tipteki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır. Bu özelliğin varsayılan değeri **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | OLE denetimlerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri alır. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Renderleme için anti-aliasing kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Yüksek kalite (yani yavaş) renderleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | Belgeyi görüntülemek için hedef makinedeki yazı tiplerinin kullanılıp kullanılmayacağını gösteren bayrak. Bu bayrak **true** olarak ayarlandığında, [FontFormat](./get_fontformat/) ve [ExportEmbeddedFonts](./get_exportembeddedfonts/) özellikleri etkisiz olur, ayrıca [ResourceSavingCallback](./get_resourcesavingcallback/) yazı tipleri için tetiklenmez. Varsayılan **false**. |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) için ayarlayıcı. |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Renklerin nasıl işlendiğini belirleyen bir değeri ayarlar. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String\&) | style.css dosyasındaki tüm sınıf adlarına eklenen önek belirtir. Varsayılan değer **%\"aw\"**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) için ayarlayıcı. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) için ayarlayıcı. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 3D efektlerin nasıl render edildiğini belirleyen bir değeri ayarlar. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | [Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding](./get_encoding/) için ayarlayıcı. |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss](./get_exportembeddedcss/) için ayarlayıcı. |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts](./get_exportembeddedfonts/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg](./get_exportembeddedsvg/). |
| [set_ExportFormFields](./set_exportformfields/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields](./get_exportformfields/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat](./get_fontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/) için ayarlayıcı. |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **false**'dır. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Metafile render seçeneklerini belirtmeye izin verir. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | [NumeralFormat](../numeralformat/) sayısal karakterlerin işlenmesi için ayarlar. Varsayılan olarak Avrupa rakamları kullanılır. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput](./get_optimizeoutput/). |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment](./get_pagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins](./get_pagemargins/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/) için ayarlayıcı. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Bir belge sabit sayfa HTML formatına dışa aktarıldığında kaynakların (görseller, yazı tipleri ve css) nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği biçimi belirtir. Sadece [HtmlFixed](../../aspose.words/saveformat/) olabilir. |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Sayfaların etrafındaki kenarlığın gösterilip gösterilmeyeceğini belirtir. Varsayılan **true**. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Belirli tipteki alanların, belge sabit sayfa formatına kaydedilmeden önce güncellenip güncellenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **true**'dır. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | OLE kontrollerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri ayarlar. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts](./get_usetargetmachinefonts/). |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
