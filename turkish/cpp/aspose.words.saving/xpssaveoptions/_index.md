---
title: "Aspose::Words::Saving::XpsSaveOptions sınıfı"
linktitle: "XpsSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XpsSaveOptions sınıfı. Bir belgeyi Xps formatında kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi için C++ belgelerindeki makaleyi ziyaret edin."
type: docs
weight: 38000
url: /tr/cpp/aspose.words.saving/xpssaveoptions/
---
## XpsSaveOptions class


Bir belgeyi [Xps](../../aspose.words/saveformat/) formatında kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi için [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) belgelerindeki makaleyi ziyaret edin.

```cpp
class XpsSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Belirtilen kaydetme formatı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Verilen dosya adında belirtilen dosya uzantısı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Bir belge kaydedildiğinde TrueType yazı tiplerini gömerek PostScript konturlarıyla yazı tiplerinin gömülmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Renklerin nasıl render edildiğini belirleyen bir değeri alır. |
| [get_CompressionLevel](./get_compressionlevel/)() const | Belgeyi kaydetmek için kullanılan sıkıştırma seviyesini belirtir. Varsayılan değer [Normal](../compressionlevel/)'dır. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Varsayılan şablona (dosya adı dahil) yolu alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**'dir. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | [DigitalSignatureDetails](../digitalsignaturedetails/) nesnesini alır veya ayarlar; belgeyi imzalamak için kullanılır. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 3D efektlerinin nasıl işleneceğini belirleyen bir değeri alır. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | **true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Html belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri alır. Bu özelliğin varsayılan değeri **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Metafile render seçeneklerini belirtmeye izin verir. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Sayısal render için kullanılan [NumeralFormat](../numeralformat/) değerini alır. Varsayılan olarak Avrupa sayıları kullanılır. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Bayrak, çıktının optimize edilmesinin gerekip gerekmediğini gösterir. Bu bayrak ayarlandığında gereksiz iç içe kanvaslar ve boş kanvaslar kaldırılır, aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not: Bu özellik **true** olarak ayarlanırsa içerik görüntüleme doğruluğu etkilenebilir. Varsayılan **false**'tur. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Anahat seçeneklerini belirtmeye izin verir. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Render edilecek sayfaları alır veya ayarlar. Varsayılan, belgede bulunan tüm sayfalardır. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | **true** olduğunda, uygulanabilir yerlerde çıktıyı güzel biçimlendirir. Varsayılan değer **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Bir belge kaydedilirken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [get_SaveFormat](./get_saveformat/)() override | Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. Yalnızca [Xps](../../aspose.words/saveformat/) olabilir. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Yazı tipi özniteliklerinin kullanılan karakter koduna göre değiştirilip değiştirilmeyeceğini belirler. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Belgenin sabit sayfa formatına kaydedilmeden önce belirli tipteki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır. Bu özelliğin varsayılan değeri **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | OLE denetimlerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri alır. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Renderleme için anti-aliasing kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/) aracılığıyla belirtilmişse, belgenin kitapçık baskı düzeniyle kaydedilip kaydedilmeyeceğini belirten bir boolean değeri alır veya ayarlar. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Yüksek kalite (yani yavaş) renderleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) için ayarlayıcı. |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Renklerin nasıl işlendiğini belirleyen bir değeri ayarlar. |
| [set_CompressionLevel](./set_compressionlevel/)(Aspose::Words::Saving::CompressionLevel) | [Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel](./get_compressionlevel/) için ayarlayıcı. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) için ayarlayıcı. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) için ayarlayıcı. |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::DigitalSignatureDetails\>\&) | [Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/) için ayarlayıcı. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 3D efektlerin nasıl render edildiğini belirleyen bir değeri ayarlar. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/) için ayarlayıcı. |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **false**'dır. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Metafile render seçeneklerini belirtmeye izin verir. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | [NumeralFormat](../numeralformat/) sayısal karakterlerin işlenmesi için ayarlar. Varsayılan olarak Avrupa rakamları kullanılır. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/) için ayarlayıcı. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/) için ayarlayıcı. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | [Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat](./get_saveformat/) için ayarlayıcı. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Belirli tipteki alanların, belge sabit sayfa formatına kaydedilmeden önce güncellenip güncellenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **true**'dır. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | OLE kontrollerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri ayarlar. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | [Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/) için ayarlayıcı. |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |
| [XpsSaveOptions](./xpssaveoptions/)() | Bu sınıfın yeni bir örneğini başlatır; bu örnek belgeyi [Xps](../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir. |
| [XpsSaveOptions](./xpssaveoptions/)(Aspose::Words::SaveFormat) | Bu sınıfın yeni bir örneğini başlatır; bu örnek belgeyi [Xps](../../aspose.words/saveformat/) veya [OpenXps](../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir. |

## Örnekler



Kaydedilen bir XPS belgesinin taslak (outline) içinde görünecek başlık seviyelerinin nasıl sınırlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Seviye 1, 2 ve ardından 3 olan başlıkları, TOC (İçindekiler) girdileri olarak ekleyin.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// \"XpsSaveOptions\" nesnesi oluşturun; bu nesneyi belgenin \"Save\" yöntemine geçebiliriz
// bu yöntemin belgeyi .XPS'ye nasıl dönüştürdüğünü değiştirmek için.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Çıktı XPS belgesi bir taslak, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu içerecektir.
// Bu taslaktaki bir girdiye tıklamak, ilgili başlığın konumuna götürür.
// \"HeadingsOutlineLevels\" özelliğini \"2\" olarak ayarlayın; böylece seviyeleri 2'nin üzerindeki tüm başlıklar taslaktan dışlanır.
// Yukarıda eklediğimiz son iki başlık görünmeyecek.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Ayrıca Bakınız

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
