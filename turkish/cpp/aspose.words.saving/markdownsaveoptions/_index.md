---
title: "Aspose::Words::Saving::MarkdownSaveOptions sınıfı"
linktitle: "MarkdownSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions sınıfı. Bir belgeyi Markdown formatında kaydederken ek seçenekleri belirtmek için sınıf. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class


Belgeyi [Markdown](../../aspose.words/saveformat/) formatında kaydederken ek seçenekleri belirtmek için sınıf. Daha fazla bilgi edinmek için [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) belge makalesini ziyaret edin.

```cpp
class MarkdownSaveOptions : public Aspose::Words::Saving::TxtSaveOptionsBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Belirtilen kaydetme formatı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Verilen dosya adında belirtilen dosya uzantısı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Bir belge kaydedildiğinde TrueType yazı tiplerini gömerek PostScript konturlarıyla yazı tiplerinin gömülmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Varsayılan şablona (dosya adı dahil) yolu alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**'dir. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 3D efektlerinin nasıl işleneceğini belirleyen bir değeri alır. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/)() const | Boş paragrafların Markdown'a nasıl dışa aktarılacağını belirtir. Varsayılan değer [EmptyLine](../markdownemptyparagraphexportmode/). |
| [get_Encoding](../txtsaveoptionsbase/get_encoding/)() const | Metin formatlarında dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer **Encoding.UTF8**'dir. |
| [get_ExportAsHtml](./get_exportashtml/)() const | Markdown'a ham HTML olarak dışa aktarılacak öğeleri belirtmeye izin verir. Varsayılan değer [None](../markdownexportashtml/). |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | **true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur. |
| [get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/)() const | Üstbilgi ve altbilgilerin metin formatlarına nasıl dışa aktarılacağını belirtir. Varsayılan değer [PrimaryOnly](../txtexportheadersfootersmode/)'dır. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Görüntülerin çıktı dosyasına Base64 formatında kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer **false**. |
| [get_ExportUnderlineFormatting](./get_exportunderlineformatting/)() const | Altı çizili metin biçimlendirmesini iki artı işareti "++" dizisi olarak dışa aktarılıp aktarılmayacağını gösteren bir boolean değer alır veya ayarlar. Varsayılan değer **false**. |
| [get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/)() const | Dışa aktarım sırasında sayfa sonlarının korunup korunmayacağını belirtmeye olanak tanır. Varsayılan değer **false**'dur. |
| [get_ImageResolution](./get_imageresolution/)() const | Markdown'a dışa aktarırken görüntüler için çıktı çözünürlüğünü belirtir. Varsayılan **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Bir belge [Markdown](../../aspose.words/saveformat/) formatında kaydedildiğinde görüntülerin nasıl kaydedileceğini kontrol etmeye izin verir. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Bir belgeyi [Markdown](../../aspose.words/saveformat/) formatına dışa aktarırken görüntülerin kaydedileceği fiziksel klasörü belirtir. Varsayılan boş bir dizedir. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Belgeye yazılan görüntü URI'lerini oluşturmak için kullanılan klasör adını belirtir. Varsayılan boş bir dizedir. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar. |
| [get_LinkExportMode](./get_linkexportmode/)() const | Bağlantıların çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer [Auto](../markdownlinkexportmode/). |
| [get_ListExportMode](./get_listexportmode/)() const | Liste öğelerinin çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer [MarkdownSyntax](../markdownlistexportmode/). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri alır. Bu özelliğin varsayılan değeri **false**. |
| [get_OfficeMathExportMode](./get_officemathexportmode/)() const | OfficeMath'in çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer [Text](../markdownofficemathexportmode/). |
| [get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/)() const | Metin formatlarında dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | **true** olduğunda, uygulanabilir yerlerde çıktıyı güzel biçimlendirir. Varsayılan değer **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Bir belge kaydedilirken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Bir belge [Markdown](../../aspose.words/saveformat/) formatına dışa aktarıldığında kaynakların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [get_SaveFormat](./get_saveformat/)() override | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği formatı belirtir. Sadece [Markdown](../../aspose.words/saveformat/) olabilir. |
| [get_TableContentAlignment](./get_tablecontentalignment/)() const | Tablolardaki içeriklerin [Markdown](../../aspose.words/saveformat/) formatına dışa aktarılırken nasıl hizalanacağını belirten bir değeri alır veya ayarlar. Varsayılan değer [Auto](../tablecontentalignment/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
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
| [MarkdownSaveOptions](./markdownsaveoptions/)() | Bu sınıfın yeni bir örneğini başlatır; bu örnek bir belgeyi [Markdown](../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir. |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) için ayarlayıcı. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) için ayarlayıcı. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) için ayarlayıcı. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 3D efektlerin nasıl render edildiğini belirleyen bir değeri ayarlar. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_EmptyParagraphExportMode](./set_emptyparagraphexportmode/)(Aspose::Words::Saving::MarkdownEmptyParagraphExportMode) | [Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/) için ayarlayıcı. |
| [set_Encoding](../txtsaveoptionsbase/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | [Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding](../txtsaveoptionsbase/get_encoding/) için ayarlayıcı. |
| [set_ExportAsHtml](./set_exportashtml/)(Aspose::Words::Saving::MarkdownExportAsHtml) | [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml](./get_exportashtml/) için ayarlayıcı. |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](../txtsaveoptionsbase/set_exportheadersfootersmode/)(Aspose::Words::Saving::TxtExportHeadersFootersMode) | [Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/) için ayarlayıcı. |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/) için ayarlayıcı. |
| [set_ExportUnderlineFormatting](./set_exportunderlineformatting/)(bool) | Ayarlayıcı [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting](./get_exportunderlineformatting/). |
| [set_ForcePageBreaks](../txtsaveoptionsbase/set_forcepagebreaks/)(bool) | Ayarlayıcı [Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Ayarlayıcı [Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Bir belge [Markdown](../../aspose.words/saveformat/) formatında kaydedildiğinde görüntülerin nasıl kaydedileceğini kontrol etmeye izin verir. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_LinkExportMode](./set_linkexportmode/)(Aspose::Words::Saving::MarkdownLinkExportMode) | Ayarlayıcı [Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode](./get_linkexportmode/). |
| [set_ListExportMode](./set_listexportmode/)(Aspose::Words::Saving::MarkdownListExportMode) | Ayarlayıcı [Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode](./get_listexportmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **false**'dır. |
| [set_OfficeMathExportMode](./set_officemathexportmode/)(Aspose::Words::Saving::MarkdownOfficeMathExportMode) | Ayarlayıcı [Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode](./get_officemathexportmode/). |
| [set_ParagraphBreak](../txtsaveoptionsbase/set_paragraphbreak/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Bir belge [Markdown](../../aspose.words/saveformat/) formatına dışa aktarıldığında kaynakların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği formatı belirtir. Sadece [Markdown](../../aspose.words/saveformat/) olabilir. |
| [set_TableContentAlignment](./set_tablecontentalignment/)(Aspose::Words::Saving::TableContentAlignment) | Ayarlayıcı [Aspose::Words::Saving::MarkdownSaveOptions::get_TableContentAlignment](./get_tablecontentalignment/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Belirli tipteki alanların, belge sabit sayfa formatına kaydedilmeden önce güncellenip güncellenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **true**'dır. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | OLE kontrollerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri ayarlar. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [TxtSaveOptionsBase](../txtsaveoptionsbase/txtsaveoptionsbase/)() |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
