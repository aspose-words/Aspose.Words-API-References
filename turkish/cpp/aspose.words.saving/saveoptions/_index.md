---
title: "Aspose::Words::Saving::SaveOptions sınıfı"
linktitle: "SaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions sınıfı. Bu, bir belgeyi belirli bir biçime kaydederken kullanıcıya ek seçenekler belirtme imkanı tanıyan sınıflar için soyut bir temel sınıftır. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 29000
url: /tr/cpp/aspose.words.saving/saveoptions/
---
## SaveOptions class


Bu, bir belgeyi belirli bir formata kaydederken ek seçenekleri belirtmesine izin veren sınıflar için soyut bir temel sınıftır. Daha fazla bilgi için, [Kaydetme Seçeneklerini Belirle](https://docs.aspose.com/words/cpp/specify-save-options/) dokümantasyon makalesini ziyaret edin.

```cpp
class SaveOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [CreateSaveOptions](./createsaveoptions/)(Aspose::Words::SaveFormat) | Belirtilen kaydetme formatı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| static [CreateSaveOptions](./createsaveoptions/)(const System::String\&) | Verilen dosya adında belirtilen dosya uzantısı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| [get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/)() const | Bir belge kaydedildiğinde TrueType yazı tiplerini gömerek PostScript konturlarıyla yazı tiplerinin gömülmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [get_CustomTimeZoneInfo](./get_customtimezoneinfo/)() const | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [get_DefaultTemplate](./get_defaulttemplate/)() const | Varsayılan şablona (dosya adı dahil) yolu alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**'dir. |
| [get_Dml3DEffectsRenderingMode](./get_dml3deffectsrenderingmode/)() const | 3D efektlerinin nasıl işleneceğini belirleyen bir değeri alır. |
| virtual [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DmlRenderingMode](./get_dmlrenderingmode/)() const | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_ExportGeneratorName](./get_exportgeneratorname/)() const | **true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur. |
| [get_ImlRenderingMode](./get_imlrenderingmode/)() const | Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar. |
| [get_MemoryOptimization](./get_memoryoptimization/)() const | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri alır. Bu özelliğin varsayılan değeri **false**. |
| [get_PrettyFormat](./get_prettyformat/)() const | **true** olduğunda, uygulanabilir yerlerde çıktıyı güzel biçimlendirir. Varsayılan değer **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Bir belge kaydedilirken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| virtual [get_SaveFormat](./get_saveformat/)() | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. |
| [get_TempFolder](./get_tempfolder/)() const | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_UpdateAmbiguousTextFont](./get_updateambiguoustextfont/)() const | Yazı tipi özniteliklerinin kullanılan karakter koduna göre değiştirilip değiştirilmeyeceğini belirler. |
| [get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/)() const | [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer **false**;. |
| [get_UpdateFields](./get_updatefields/)() const | Belgenin sabit sayfa formatına kaydedilmeden önce belirli tipteki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır. Bu özelliğin varsayılan değeri **true**. |
| [get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/)() const | [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/)() const | [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateOleControlImages](./get_updateolecontrolimages/)() const | OLE denetimlerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri alır. |
| [get_UseAntiAliasing](./get_useantialiasing/)() const | Renderleme için anti-aliasing kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseHighQualityRendering](./get_usehighqualityrendering/)() const | Yüksek kalite (yani yavaş) renderleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](./set_allowembeddingpostscriptfonts/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](./set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](./get_customtimezoneinfo/). |
| [set_DefaultTemplate](./set_defaulttemplate/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](./get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](./set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 3D efektlerin nasıl render edildiğini belirleyen bir değeri ayarlar. |
| virtual [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](./set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](./get_dmlrenderingmode/). |
| [set_ExportGeneratorName](./set_exportgeneratorname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](./get_exportgeneratorname/). |
| [set_ImlRenderingMode](./set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](./get_imlrenderingmode/). |
| [set_MemoryOptimization](./set_memoryoptimization/)(bool) | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **false**'dır. |
| [set_PrettyFormat](./set_prettyformat/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](./get_prettyformat/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](./get_progresscallback/). |
| virtual [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](./set_updateambiguoustextfont/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](./get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](./set_updatecreatedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/). |
| [set_UpdateFields](./set_updatefields/)(bool) | Belirli tipteki alanların, belge sabit sayfa formatına kaydedilmeden önce güncellenip güncellenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **true**'dır. |
| [set_UpdateLastPrintedProperty](./set_updatelastprintedproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](./set_updatelastsavedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](./set_updateolecontrolimages/)(bool) | OLE kontrollerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri ayarlar. |
| [set_UseAntiAliasing](./set_useantialiasing/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](./get_useantialiasing/). |
| [set_UseHighQualityRendering](./set_usehighqualityrendering/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](./get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## Örnekler



.epub formatında bir belge kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Kaydedeceğimiz bir belgenin kodlamasını belirtmek için bir SaveOptions nesnesi kullanın.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Varsayılan olarak, çıkış .epub belgesi tüm içeriğini tek bir HTML bölümünde tutar.
// Bir bölme ölçütü, belgeyi birden fazla HTML bölümüne ayırmamıza olanak tanır.
// Belgeyi başlık paragraflarına bölmek için ölçütleri ayarlayacağız.
// Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için faydalıdır.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Belge özelliklerini dışa aktarmak istediğimizi belirtin.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
