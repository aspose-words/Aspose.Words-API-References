---
title: "Aspose::Words::Saving::HtmlSaveOptions class"
linktitle: "HtmlSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions sınıfı. Bir belgeyi Html, Mhtml, Epub, Azw3 veya Mobi formatına kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Bir belgeyi [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) veya [Mobi](../../aspose.words/saveformat/) formatına kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi edinmek için [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) belge makalesini ziyaret edin.

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Belirtilen kaydetme formatı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Verilen dosya adında belirtilen dosya uzantısı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Bir belge kaydedildiğinde TrueType yazı tiplerini gömerek PostScript konturlarıyla yazı tiplerinin gömülmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Paragrafların negatif sol ve sağ girintilerinin HTML, MHTML veya EPUB olarak kaydedilirken normalleştirilip normalleştirilmeyeceğini belirtir. Varsayılan değer **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Tüm CSS sınıf adlarına eklenen bir önek belirtir. Varsayılan değer boş bir dizedir ve oluşturulan CSS sınıf adlarında ortak bir önek bulunmaz. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde CSS stillerinin nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Bir belge HTML olarak dışa aktarıldığında yazılan Cascading [Style](../../aspose.words/style/) Sheet (CSS) dosyasının yolunu ve adını belirtir. Varsayılan değer boş bir dizedir. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | CSS (Cascading [Style](../../aspose.words/style/) Sheet) stillerinin HTML, MHTML veya EPUB'a nasıl dışa aktarılacağını belirtir. Varsayılan değer HTML/MHTML için [Inline](../cssstylesheettype/), EPUB için [External](../cssstylesheettype/) dir. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Varsayılan şablona (dosya adı dahil) yolu alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**'dir. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 3D efektlerinin nasıl işleneceğini belirleyen bir değeri alır. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Bir belge HTML veya EPUB olarak kaydedildiğinde belge bölümlerinin nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Belgenin [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) veya [Azw3](../../aspose.words/saveformat/) formatına kaydedilirken nasıl bölüneceğini belirtir. Varsayılan değer HTML için [None](../documentsplitcriteria/), EPUB ve AZW3 için [HeadingParagraph](../documentsplitcriteria/) dir. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Belgenin bölüneceği en yüksek başlık seviyesini belirtir. Varsayılan değer **%2**'dir. |
| [get_Encoding](./get_encoding/)() const | HTML, MHTML veya EPUB'a dışa aktarılırken kullanılacak kodlamayı belirtir. Varsayılan değer **new UTF8Encoding(false)** (BOM olmadan UTF-8)'dir. |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | MHTML belgelerinde bulunan kaynakları (görseller, yazı tipleri, CSS) referanslamak için CID (Content-ID) URL'lerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değer **false**'tur. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Yerleşik ve özel belge özelliklerinin HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**'tur. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Açılır menü form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer **false**'tur. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Yazı tipi kaynaklarının HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**'tur. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Yazı tipi kaynaklarının Base64 kodlamasıyla HTML'ye gömülüp gömülmeyeceğini belirtir. Varsayılan değer **false**'tur. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | **true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Üstbilgi ve altbilgilerin HTML, MHTML veya EPUB'a nasıl çıktılanacağını belirtir. Varsayılan değer HTML/MHTML için [PerSection](../exportheadersfootersmode/), EPUB için [None](../exportheadersfootersmode/) dir. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Görsellerin çıktı HTML, MHTML veya EPUB'a Base64 formatında kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer **false**'tur. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Dil bilgilerinin HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**'tur. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Liste etiketlerinin HTML, MHTML veya EPUB'a nasıl çıktılanacağını kontrol eder. Varsayılan değer [Auto](../exportlistlabels/)'dır. |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Orijinal URL'nin bağlantılı görsellerin URL'si olarak kullanılıp kullanılmayacağını belirtir. Varsayılan değer **false**'tur. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Sayfa kenar boşluklarının HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**'tur. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Sayfa ayarının HTML, MHTML veya EPUB formatına aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | HTML, MHTML veya EPUB olarak kaydederken yazı tipi boyutlarının göreceli birimlerde çıktılanıp çıktılanmayacağını belirtir. Varsayılan değer **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | HTML, MHTML veya EPUB olarak kaydederken roundtrip bilgisinin yazılıp yazılmayacağını belirtir. Varsayılan değer HTML için **true**, MHTML ve EPUB için **false**. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | [Shape](../../aspose.words.drawing/shape/) düğümlerinin HTML, MHTML, EPUB veya AZW3 olarak kaydederken SVG görüntülerine dönüştürülüp dönüştürülmeyeceğini denetler. Varsayılan değer **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Metin giriş form alanlarının HTML veya MHTML olarak nasıl kaydedileceğini denetler. Varsayılan değer **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | HTML, MHTML ve EPUB olarak kaydederken içindekiler tablosuna sayfa numaralarının yazılıp yazılmayacağını belirtir. Varsayılan değer **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | HTML veya MHTML olarak kaydederken DOCTYPE bildiriminin yazılıp yazılmayacağını belirtir. **true** olduğunda, kök öğeden önce belgeye bir DOCTYPE bildirimi yazar. Varsayılan değer **false**. EPUB veya HTML5 ([Html5](../htmlversion/)) olarak kaydederken DOCTYPE bildirimi her zaman yazılır. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | HTML, MHTML veya EPUB olarak kaydederken hangi yazı tipi kaynaklarının alt kümelendirilmesi gerektiğini denetler. Varsayılan değer **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde yazı tiplerinin nasıl kaydedileceğini denetlemeye olanak tanır. |
| [get_FontsFolder](./get_fontsfolder/)() const | Bir belge HTML olarak dışa aktarıldığında yazı tiplerinin kaydedileceği fiziksel klasörü belirtir. Varsayılan değer boş bir dizedir. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | HTML belgesine yazılan yazı tipi URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer boş bir dizedir. |
| [get_HtmlVersion](./get_htmlversion/)() const | Belgenin HTML veya MHTML olarak kaydedilirken kullanılacak HTML standardı sürümünü belirtir. Varsayılan değer [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | HTML, MHTML veya EPUB olarak dışa aktarırken görüntüler için çıkış çözünürlüğünü belirtir. Varsayılan değer **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde görüntülerin nasıl kaydedileceğini denetlemeye olanak tanır. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Bir belge HTML formatına dışa aktarılırken görüntülerin kaydedileceği fiziksel klasörü belirtir. Varsayılan değer boş bir dizedir. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer boş bir dizedir. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri alır. Bu özelliğin varsayılan değeri **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | HTML, MHTML veya EPUB olarak dışa aktarılırken metafile'ların hangi formatta kaydedileceğini belirtir. Varsayılan değer [Png](../htmlmetafileformat/)'dir; bu, metafile'ların raster PNG görüntülerine render edildiği anlamına gelir. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | EPUB, MOBI veya AZW3 formatlarına dışa aktarırken gezinme haritasına doldurulan başlıkların maksimum seviyesini belirtir. Varsayılan değer **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | OfficeMath nesnelerinin HTML, MHTML veya EPUB olarak nasıl dışa aktarılacağını denetler. Varsayılan değer [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | **true** olduğunda, uygulanabilir yerlerde çıktıyı güzel biçimlendirir. Varsayılan değer **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Bir belge kaydedilirken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Bağlantılardan JavaScript'in kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Ters eğik çizgi karakterlerinin yen işaretiyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Belirtilen, belgede kullanılan yazı tipi ailesi adlarının HTML tabanlı formatlara yazılırken [FontSettings](../../aspose.words/document/get_fontsettings/) göre çözülüp yerine konulup konulmayacağını belirtir. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Bir belge HTML'ye dışa aktarıldığında görüntüler, yazı tipleri ve harici CSS gibi tüm kaynakların kaydedildiği fiziksel klasörü belirtir. Varsayılan değer boş bir dizedir. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | HTML belgesine yazılan tüm kaynakların URI'larını oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer boş bir dizedir. |
| [get_SaveFormat](./get_saveformat/)() override | Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) veya [Mobi](../../aspose.words/saveformat/) olabilir. |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | HTML, MHTML veya EPUB'a dışa aktarırken görüntülerin Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmeyeceğini belirtir. Varsayılan değer **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Tablo, satır ve hücre genişliklerinin HTML, MHTML veya EPUB'a nasıl dışa aktarılacağını kontrol eder. Varsayılan değer [All](../htmlelementsizeoutputmode/). |
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
| [HtmlSaveOptions](./htmlsaveoptions/)() | Bu sınıfın yeni bir örneğini başlatır; bu örnek belgeyi [Html](../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir. |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Bu sınıfın yeni bir örneğini başlatır; bu örnek belgeyi [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) veya [Mobi](../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) için ayarlayıcı. |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/) için ayarlayıcı. |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/) için ayarlayıcı. |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde CSS stillerinin nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/) için ayarlayıcı. |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/) için ayarlayıcı. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) için ayarlayıcı. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) için ayarlayıcı. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 3D efektlerin nasıl render edildiğini belirleyen bir değeri ayarlar. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | Bir belge HTML veya EPUB olarak kaydedildiğinde belge bölümlerinin nasıl kaydedileceğini kontrol etmeyi sağlar. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/). |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/). |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde yazı tiplerinin nasıl kaydedileceğini denetlemeye olanak tanır. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Bir belge HTML, MHTML veya EPUB olarak kaydedildiğinde görüntülerin nasıl kaydedileceğini denetlemeye olanak tanır. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **false**'dır. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Bağlantılardan JavaScript'in kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Ayarlayıcı [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Belirli tipteki alanların, belge sabit sayfa formatına kaydedilmeden önce güncellenip güncellenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **true**'dır. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | OLE kontrollerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri ayarlar. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
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


Bağlantılı görüntülerin .html olarak kaydedildikten sonra depolanacağı klasörün nasıl belirtileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarmak için bir seçenek ayarlayın.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Ayrıca Bakınız

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
