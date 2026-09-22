---
title: "Aspose::Words::Saving::PdfSaveOptions sınıfı"
linktitle: "PdfSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions sınıfı. Bir belgeyi PDF formatına kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 25000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


Bir belgeyi [Pdf](../../aspose.words/saveformat/) formatında kaydederken ek seçenekleri belirtmek için kullanılabilir. Daha fazla bilgi edinmek için [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) dokümantasyon makalesini ziyaret edin.

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | Bu nesnenin derin bir klonunu oluşturur. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Belirtilen kaydetme formatı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Verilen dosya adında belirtilen dosya uzantısı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | Ek metin konumlandırma operatörlerinin yazılıp yazılmayacağını belirten bir bayrak. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Bir belge kaydedildiğinde TrueType yazı tiplerini gömerek PostScript konturlarıyla yazı tiplerinin gömülmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | Eklerin PDF belgesine nasıl gömüleceğini belirleyen bir değeri alır veya ayarlar. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | Belgenin arka planına yerleştirilen grafiklerin önbelleğe alınıp alınmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Renklerin nasıl render edildiğini belirleyen bir değeri alır. |
| [get_Compliance](./get_compliance/)() const | Çıktı belgeleri için PDF standartları uyumluluk seviyesini belirtir. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | Ana metin akışındaki dipnot/sonnot referanslarını aktif köprüye dönüştürüp dönüştürmeyeceğini belirtir. Tıklandığında köprü ilgili dipnot/sonnota yönlendirilir. Varsayılan **false** değeridir. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) öğelerinin PDF dosyasına nasıl dışa aktarılacağını belirleyen bir değeri alır veya ayarlar. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Tarih/saat alanları için kullanılan özel yerel saat dilimini alır veya ayarlar. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Varsayılan şablona (dosya adı dahil) yolu alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**'dir. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Çıktı PDF belgesinin imzalanmasıyla ilgili ayrıntıları alır veya ayarlar. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | Pencerenin başlık çubuğunun, belge bilgi sözlüğündeki Title girişinden alınan belge başlığını gösterip göstermeyeceğini belirten bir bayrak. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 3D efektlerinin nasıl işleneceğini belirleyen bir değeri alır. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | DrawingML efektlerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | DrawingML şekillerinin nasıl işleneceğini belirleyen bir değeri alır veya ayarlar. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | Alt örnekleme seçeneklerini belirtmeye izin verir. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | Yazı tiplerinin ortaya çıkan PDF belgelerine nasıl gömüleceğini kontrol eder. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | Çıktı PDF belgesinin şifrelenmesiyle ilgili ayrıntıları alır veya ayarlar. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | Belge yapısının dışa aktarılıp aktarılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | Kayan şekillerin belge yapısında satır içi etiketler olarak dışa aktarılıp aktarılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | **true** olduğunda, Aspose.Words'un adının ve sürümünün oluşturulan dosyalara gömülmesini sağlar. Varsayılan değer **true**'dur. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | Metin dilini dışa aktarmak için belge yapısında bir "Span" etiketi oluşturulup oluşturulmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | Paragraf grafiğinin bir artefakt olarak işaretlenip işaretlenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | Yazı tipi gömme modunu belirtir. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | PDF içinde belirli Microsoft Word form alanı davranışını taklit eden betiklerin üretilip üretilmeyeceğini belirtir. Varsayılan **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | Üstbilgi/altbilgi içindeki yer imlerinin nasıl dışa aktarılacağını belirler. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | PDF belgesindeki görüntüler için renk uzayının nasıl seçileceğini belirtir. |
| [get_ImageCompression](./get_imagecompression/)() const | Belgedeki tüm görüntüler için kullanılacak sıkıştırma türünü belirtir. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar. |
| [get_InterpolateImages](./get_interpolateimages/)() const | Uyumlu bir okuyucu tarafından görüntü enterpolasyonunun yapılıp yapılmayacağını gösteren bir bayrak. **false** belirtildiğinde, bayrak çıktı belgesine yazılmaz ve okuyucunun varsayılan davranışı kullanılır. |
| [get_JpegQuality](./get_jpegquality/)() | PDF belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Html belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri alır. Bu özelliğin varsayılan değeri **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Metafile render seçeneklerini belirtmeye izin verir. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Sayısal render için kullanılan [NumeralFormat](../numeralformat/) değerini alır. Varsayılan olarak Avrupa sayıları kullanılır. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | Çıktı Pdf belgesindeki köprülerin yeni bir pencere (veya sekme) içinde açılmaya zorlanıp zorlanmayacağını belirleyen bir değeri alır veya ayarlar. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Bayrak, çıktının optimize edilmesinin gerekip gerekmediğini gösterir. Bu bayrak ayarlandığında gereksiz iç içe kanvaslar ve boş kanvaslar kaldırılır, aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not: Bu özellik **true** olarak ayarlanırsa içerik görüntüleme doğruluğu etkilenebilir. Varsayılan **false**'tur. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Anahat seçeneklerini belirtmeye izin verir. |
| [get_PageLayout](./get_pagelayout/)() const | Belge bir PDF okuyucusunda açıldığında kullanılacak sayfa düzenini belirtir. |
| [get_PageMode](./get_pagemode/)() const | PDF belgesinin bir PDF okuyucusunda açıldığında nasıl görüntüleneceğini belirtir. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Render edilecek sayfaları alır veya ayarlar. Varsayılan, belgede bulunan tüm sayfalardır. |
| [get_PreblendImages](./get_preblendimages/)() const | Şeffaf görüntüleri siyah arka plan rengiyle önceden karıştırıp karıştırmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | Microsoft Word form alanlarını PDF'de form alanı olarak koruyup korumayacağını veya metne dönüştürülüp dönüştürülmeyeceğini belirtir. Varsayılan **false** değeridir. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | **true** olduğunda, uygulanabilir yerlerde çıktıyı güzel biçimlendirir. Varsayılan değer **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Bir belge kaydedilirken çağrılır ve kaydetme ilerlemesiyle ilgili verileri kabul eder. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | PDF seçim form alanı kenarlığının render edilip edilmeyeceğini belirtir. |
| [get_SaveFormat](./get_saveformat/)() override | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin hangi formatta kaydedileceğini belirtir. Yalnızca [Pdf](../../aspose.words/saveformat/) olabilir. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz. |
| [get_TextCompression](./get_textcompression/)() const | Belgedeki tüm metin içeriği için kullanılacak sıkıştırma türünü belirtir. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Yazı tipi özniteliklerinin kullanılan karakter koduna göre değiştirilip değiştirilmeyeceğini belirler. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Belgenin sabit sayfa formatına kaydedilmeden önce belirli tipteki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır. Bu özelliğin varsayılan değeri **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | OLE denetimlerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri alır. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Renderleme için anti-aliasing kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/) aracılığıyla belirtilmişse, belgenin kitapçık baskı düzeniyle kaydedilip kaydedilmeyeceğini belirten bir boolean değeri alır veya ayarlar. |
| [get_UseCoreFonts](./get_usecorefonts/)() const | TrueType yazı tipleri Arial, Times New Roman, Courier New ve Symbol'ü temel PDF Type 1 yazı tipleriyle değiştirip değiştirmeyeceğini belirleyen bir değeri alır veya ayarlar. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Yüksek kalite (yani yavaş) renderleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar. |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | PDF'de form alanı adı olarak SDT kontrol Etiketi (Tag) mi yoksa Id özelliği mi kullanılacağını belirtir. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | Bir belge PDF görüntüleyicide açıldığında hangi tür yakınlaştırmanın uygulanacağını belirleyen bir değeri alır. |
| [get_ZoomFactor](./get_zoomfactor/)() const | Belge için yakınlaştırma faktörünü (yüzde olarak) belirleyen bir değeri alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | Bu sınıfın yeni bir örneğini başlatır; bu örnek belgeyi [Pdf](../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir. |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/) için ayarlayıcı. |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) için ayarlayıcı. |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/) için ayarlayıcı. |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/) için ayarlayıcı. |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Renklerin nasıl işlendiğini belirleyen bir değeri ayarlar. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | Çıktı belgeleri için PDF standartları uyumluluk seviyesini belirtir. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | Ana metin akışındaki dipnot/sonnot referanslarını aktif köprüye dönüştürüp dönüştürmeyeceğini belirtir. Tıklandığında köprü ilgili dipnot/sonnota yönlendirilir. Varsayılan **false** değeridir. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/) için ayarlayıcı. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) için ayarlayıcı. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) için ayarlayıcı. |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/) için ayarlayıcı. |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/) için ayarlayıcı. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 3D efektlerin nasıl render edildiğini belirleyen bir değeri ayarlar. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/) için ayarlayıcı. |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | Alt örnekleme seçeneklerini belirtmeye izin verir. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/) için ayarlayıcı. |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/) için ayarlayıcı. |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/) için ayarlayıcı. |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/) için ayarlayıcı. |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/) için ayarlayıcı. |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/) için ayarlayıcı. |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/) için ayarlayıcı. |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/) için ayarlayıcı. |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/). |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/). |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Belge kaydedilmeden önce bellek optimizasyonunun yapılması gerekip gerekmediğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **false**'dır. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Metafile render seçeneklerini belirtmeye izin verir. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | [NumeralFormat](../numeralformat/) sayısal karakterlerin işlenmesi için ayarlar. Varsayılan olarak Avrupa rakamları kullanılır. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/) için ayarlayıcı. |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | Belge bir PDF okuyucusunda açıldığında kullanılacak sayfa düzenini belirtir. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | PDF belgesinin bir PDF okuyucusunda açıldığında nasıl görüntüleneceğini belirtir. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Bir belge sabit sayfa formatına dışa aktarıldığında ayrı sayfaların nasıl kaydedileceğini kontrol etmeye izin verir. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/) için ayarlayıcı. |
| [set_PreblendImages](./set_preblendimages/)(bool) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/). |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin hangi formatta kaydedileceğini belirtir. Yalnızca [Pdf](../../aspose.words/saveformat/) olabilir. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Belirli tipteki alanların, belge sabit sayfa formatına kaydedilmeden önce güncellenip güncellenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri **true**'dır. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | OLE kontrollerinin sunum görüntüsünün güncellenip güncellenmeyeceğini belirleyen bir değeri ayarlar. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Ayarlayıcı [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | Ayarlayıcı [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/). |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | Bir belge PDF görüntüleyicide açıldığında uygulanacak yakınlaştırma türünü belirleyen bir değer ayarlar. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | Bir belge için yakınlaştırma faktörünü (yüzde olarak) belirleyen bir değer ayarlar. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
