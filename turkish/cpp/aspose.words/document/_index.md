---
title: "Aspose::Words::Document sınıfı"
linktitle: "Belge"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document sınıfı. Bir Word belgesini temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 20000
url: /tr/cpp/aspose.words/document/
---
## Document class


Bir Word belgesini temsil eder. Daha fazla bilgi edinmek için [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptAllRevisions](./acceptallrevisions/)() | Belgedeki tüm izlenen değişiklikleri kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Belgenin sonunu ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Belgenin başlangıcını ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Belirtilen belgeyi bu belgenin sonuna ekler. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Belirtilen belgeyi bu belgenin sonuna ekler. |
| [Cleanup](./cleanup/)() | Belgeden kullanılmayan stilleri ve listeleri temizler. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | Belgeden kullanılmayan stilleri ve listeleri, verilen [CleanupOptions](../cleanupoptions/) öğesine bağlı olarak temizler. |
| [Clone](./clone/)() | [Document](./) nesnesinin derin kopyasını gerçekleştirir. |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | Bu belgeyi başka bir belgeyle karşılaştırır ve değişiklikleri düzenleme ve biçim revizyonları sayısı olarak [Revision](../revision/) üretir. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Bu belgeyi başka bir belgeyle karşılaştırır ve değişiklikleri düzenleme ve biçim revizyonları sayısı olarak [Revision](../revision/) üretir. [CompareOptions](../../aspose.words.comparing/compareoptions/) kullanarak karşılaştırma seçeneklerini belirtmeye olanak tanır. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | Belirtilen şablondan bir belgeye stilleri kopyalar. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Belirtilen şablondan bir belgeye stilleri kopyalar. |
| [Document](./document/)() | Boş bir Word belgesi oluşturur. |
| [Document](./document/)(const System::String\&) | Varolan bir belgeyi dosyadan açar. Dosya formatını otomatik olarak algılar. |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Varolan bir belgeyi dosyadan açar. Şifreleme parolası gibi ek seçenekleri belirtmeye olanak tanır. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | Varolan bir belgeyi akıştan açar. Dosya formatını otomatik olarak algılar. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Varolan bir belgeyi akıştan açar. Şifreleme parolası gibi ek seçenekleri belirtmeye olanak tanır. |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | Belge hiçbir bölüm içermiyorsa, bir paragraf içeren bir bölüm oluşturur. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | Tablo stillerinde belirtilen biçimlendirmeyi, belgedeki tablolara doğrudan biçimlendirme olarak dönüştürür. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | Belirtilen sayfa aralığını ve verilen sayfa çıkarma seçeneklerini temsil eden [Document](./) nesnesini döndürür. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | Belirtilen sayfa aralığını temsil eden [Document](./) nesnesini döndürür. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | Belgeye ekli şablonun tam yolunu alır veya ayarlar. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | Belge her MS Word'ta açıldığında, belgedeki stillerin ekli şablondaki stillerle eşleşecek şekilde güncellenip güncellenmeyeceğini gösteren bayrağı alır veya ayarlar. |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | Belgenin arka plan şekli alınır veya ayarlanır. **null** olabilir. |
| [get_Bibliography](./get_bibliography/)() | Belgede mevcut kaynakların listesini temsil eden [Bibliography](./get_bibliography/) nesnesini alır. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Belgenin tüm yerleşik belge özelliklerini temsil eden bir koleksiyon döndürür. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | Belge uyumluluk seçeneklerine erişim sağlar (yani Word'deki **Options** iletişim kutusunun **Compatibility** sekmesinde girilen kullanıcı tercihleri). |
| [get_Compliance](./get_compliance/)() | Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca OOXML belgeleri için anlamlıdır. |
| [get_Count](../compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | Belgenin tüm özel belge özelliklerini temsil eden bir koleksiyon döndürür. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | Custom XML Data Storage Parts koleksiyonunu alır veya ayarlar. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | Varsayılan sekme durakları arasındaki aralığı (puan cinsinden) alır veya ayarlar. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | Bu belge için dijital imzalar koleksiyonunu ve bunların doğrulama sonuçlarını alır. |
| [get_Document](../documentbase/get_document/)() const override | Bu örneği alır. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Bu belgede dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sağlar. |
| [get_FieldOptions](./get_fieldoptions/)() | Belgede alan işleme kontrol seçeneklerini temsil eden bir [FieldOptions](../../aspose.words.fields/fieldoptions/) nesnesini alır. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FirstSection](./get_firstsection/)() | Belgedeki ilk bölümü alır. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [get_FontSettings](./get_fontsettings/)() const | Belge yazı tipi ayarlarını alır veya ayarlar. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Bu belgede dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sağlar. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | Belgede tanımlanan dipnot/dipnot ayırıcılarına erişim sağlar. |
| [get_Frameset](./get_frameset/)() const | Bu belge bir çerçeve sayfasını temsil ediyorsa bir [Frameset](./get_frameset/) örneği döndürür. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | Bu belge veya şablon içindeki sözlük belgesini alır veya ayarlar. Sözlük belgesi, bir belgede tanımlanan AutoText, AutoCorrect ve Building Block girişleri için bir depolamadır. |
| [get_GrammarChecked](./get_grammarchecked/)() | Belge dilbilgisi için kontrol edilmişse **true** döndürür. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_HasMacros](./get_hasmacros/)() | Belgenin bir VBA projesi (makrolar) varsa **true** döndürür. |
| [get_HasRevisions](./get_hasrevisions/)() | Belgenin izlenen değişiklikleri varsa **true** döndürür. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | Belge heceleme seçeneklerine erişim sağlar. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | Kelime sayımı istatistiklerine metin kutularını, dipnotları ve son notları dahil edilip edilmeyeceğini belirtir. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_JustificationMode](./get_justificationmode/)() | Belgenin karakter aralığı ayarlamasını alır veya ayarlar. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_LastSection](./get_lastsection/)() | Belgedeki son bölümü alır. |
| [get_LayoutOptions](./get_layoutoptions/)() const | Bu belgenin yerleşim sürecini kontrol eden seçenekleri temsil eden bir [LayoutOptions](../../aspose.words.layout/layoutoptions/) nesnesi alır. |
| [get_Lists](../documentbase/get_lists/)() const | Belgede kullanılan liste biçimlendirmesine erişim sağlar. |
| [get_MailMerge](./get_mailmerge/)() | Belge için posta birleştirme işlevselliğini temsil eden bir [MailMerge](../../aspose.words.mailmerging/mailmerge/) nesnesi döndürür. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | Bir belge için tüm posta birleştirme bilgilerini içeren nesneyi alır veya ayarlar. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | Belgede bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| [get_NodeType](./get_nodetype/)() const override | [Document](../nodetype/) döndürür. |
| [get_OriginalFileName](./get_originalfilename/)() const | Belgenin orijinal dosya adını alır. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | Bu nesneye yüklü olan orijinal belgenin formatını alır. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | "unknown relationships" kullanılarak OOXML paketine bağlanan özel bölümlerin (keyfi içerik) koleksiyonunu alır veya ayarlar. |
| [get_PageColor](../documentbase/get_pagecolor/)() | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, [BackgroundShape](../documentbase/get_backgroundshape/) özelliğinin daha basit bir sürümüdür. |
| [get_PageCount](./get_pagecount/)() | En son sayfa yerleşim işlemi tarafından hesaplanan belge sayfası sayısını alır. |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | Şu anda etkin olan belge koruma türünü alır. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | Kerning'in hem Latin metnine hem de noktalama işaretlerine uygulanıp uygulanmayacağını belirtir. |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | Belge için okunabilirlik puanı bilgisi sağlar. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | Microsoft Word'ün belgeyi kaydederken yorumlardan, revizyonlardan ve belge özelliklerinden tüm kullanıcı bilgilerini kaldıracağını gösteren bayrağı alır veya ayarlar. |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | Harici kaynakların nasıl yükleneceğini kontrol etmeye izin verir. |
| [get_Revisions](./get_revisions/)() | Bu belgede mevcut olan revizyonların (izlenen değişiklikler) koleksiyonunu alır. |
| [get_RevisionsView](./get_revisionsview/)() const | Belgenin orijinal mi yoksa revize edilmiş sürümüyle mi çalışılacağını gösteren değeri alır veya ayarlar. |
| [get_Sections](./get_sections/)() | Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür. |
| [get_ShadeFormData](./get_shadeformdata/)() | Form alanlarında gri gölgelendirmeyi açıp açmayacağını belirtir. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | Bu belgede dilbilgisi hatalarının gösterilip gösterilmeyeceğini belirtir. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | Bu belgede yazım hatalarının gösterilip gösterilmeyeceğini belirtir. |
| [get_SpellingChecked](./get_spellingchecked/)() | Belge yazım denetiminden geçirilmişse **true** döndürür. |
| [get_Styles](../documentbase/get_styles/)() const | Belgede tanımlı stillerin bir koleksiyonunu döndürür. |
| [get_Theme](./get_theme/)() | Bu belge için [Theme](./get_theme/) nesnesini alır. |
| [get_TrackRevisions](./get_trackrevisions/)() | Bu belge Microsoft Word'de düzenlendiğinde değişiklikler izleniyorsa doğru. |
| [get_Variables](./get_variables/)() | Bir belgeye veya şablona eklenen değişkenlerin koleksiyonunu döndürür. |
| [get_VbaProject](./get_vbaproject/)() const | [VbaProject](./get_vbaproject/) nesnesini alır veya ayarlar. |
| [get_VersionsCount](./get_versionscount/)() | DOC belgesinde depolanan belge sürümlerinin sayısını alır. |
| [get_ViewOptions](./get_viewoptions/)() | Belgenin Microsoft Word'de nasıl görüntüleneceğini kontrol etmek için seçenekler sağlar. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | Veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çeşitli belge işleme prosedürleri sırasında çağrılır. |
| [get_Watermark](./get_watermark/)() | Belge filigranına erişim sağlar. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | Görev bölmesi eklentilerinin bir listesini temsil eden bir koleksiyon döndürür. |
| [get_WriteProtection](./get_writeprotection/)() | Belge yazma koruması seçeneklerine erişim sağlar. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../nodetype/) öğesinin ilk atasını alır. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetPageInfo](./getpageinfo/)(int32_t) | Sayfa boyutunu, yönünü ve yazdırma veya oluşturma için faydalı olabilecek diğer sayfa bilgilerini alır. |
| [GetText](../compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Başka bir belgeden bir düğümü geçerli belgeye aktarır. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Başka bir belgeden bir düğümü, biçimlendirmeyi kontrol etme seçeneğiyle geçerli belgeye aktarır. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Başka bir belgeden bir düğümü, biçimlendirmeyi kontrol etme seçeneğiyle geçerli belgeye aktarır. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Belgedeki tüm paragraflarda aynı biçimlendirmeye sahip koşulları birleştirir. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Belgenin tamamında [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) öğelerinin [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) değerlerini, alan kodlarında bulunan alan türlerine karşılık gelecek şekilde değiştirir. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | Mevcut şifreyi değiştirmeden belgeyi değişikliklerden korur veya rastgele bir şifre atar. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | Belgeyi değişikliklerden korur ve isteğe bağlı olarak bir koruma şifresi ayarlar. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveBlankPages](./removeblankpages/)() | Belgedeki boş sayfaları kaldırır. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | Belgeden araç çubuğu ve klavye komut özelleştirmelerini kaldırır. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | Bu belgeden harici XML şema referanslarını kaldırır. |
| [RemoveMacros](./removemacros/)() | Belgeden tüm makroları (VBA projesi) ve ayrıca araç çubukları ile komut özelleştirmelerini kaldırır. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Belge sayfasını belirtilen ölçeğe göre bir **Graphics** nesnesine işler. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Belge sayfasını belirtilen boyuta göre bir **Graphics** nesnesine işler. |
| [Save](./save/)(const System::String\&) | Belgeyi bir dosyaya kaydeder. Uzantıdan kaydetme formatını otomatik olarak belirler. |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | Belgeyi belirtilen formatta bir dosyaya kaydeder. |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Belgeyi belirtilen kaydetme seçeneklerini kullanarak bir dosyaya kaydeder. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Belgeyi belirtilen formatı kullanarak bir akışa kaydeder. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Belgeyi belirtilen kaydetme seçeneklerini kullanarak bir akışa kaydeder. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../node/) öğesini seçer. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/). |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/). |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Ayarlayıcı [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) için ayarlayıcı. |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | Ayarlayıcı [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/). |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | Ayarlayıcı [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Ayarlayıcı [Aspose::Words::Document::get_FontSettings](./get_fontsettings/). |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Ayarlayıcı [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/). |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/). |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/). |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | Ayarlayıcı [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/). |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | Ayarlayıcı [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Belgede bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | Ayarlayıcı [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/). |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/). |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Harici kaynakların nasıl yükleneceğini kontrol etmeye izin verir. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | Ayarlayıcı [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/). |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/). |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/). |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/). |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/). |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | Ayarlayıcı [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/). |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | Ayarlayıcı [Aspose::Words::Document::get_VbaProject](./get_vbaproject/). |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Ayarlayıcı [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | Belgeye programlı olarak yaptığınız tüm sonraki değişiklikleri otomatik olarak revizyon değişiklikleri olarak işaretlemeye başlar. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | Belgeye programlı olarak yaptığınız tüm sonraki değişiklikleri otomatik olarak revizyon değişiklikleri olarak işaretlemeye başlar. |
| [StopTrackRevisions](./stoptrackrevisions/)() | Belge değişikliklerinin otomatik olarak revizyon olarak işaretlenmesini durdurur. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Tüm belgede alanların bağlantısını kaldırır. |
| [Unprotect](./unprotect/)() | Parola ne olursa olsun belgenin korumasını kaldırır. |
| [Unprotect](./unprotect/)(const System::String\&) | Doğru bir parola belirtilirse belgenin korumasını kaldırır. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | Belgedeki tüm dipnot ve sonnotların [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) özelliğini günceller. |
| [UpdateFields](./updatefields/)() | Tüm belgede alan değerlerini günceller. |
| [UpdateListLabels](./updatelistlabels/)() | Belgedeki tüm liste öğelerinin liste etiketlerini günceller. |
| [UpdatePageLayout](./updatepagelayout/)() | Belgenin sayfa düzenini yeniden oluşturur. |
| [UpdateTableLayout](./updatetablelayout/)() | Bilinen sorunları olan tablo sütun genişliklerinin yeniden hesaplanması için önceki bir yaklaşımı uygular. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | Belgenin [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) özelliğini belirtilen seçeneklere göre günceller. |
| [UpdateThumbnail](./updatethumbnail/)() | Belgenin [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) özelliğini varsayılan seçeneklerle günceller. |
| [UpdateWordCount](./updatewordcount/)() | Belgenin kelime sayısı özelliklerini günceller. |
| [UpdateWordCount](./updatewordcount/)(bool) | Belgenin kelime sayısı özelliklerini günceller, isteğe bağlı olarak [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/) özelliğini de günceller. |
## Açıklamalar


Aspose.Words kütüphanesinde [Document](./) merkezi bir nesnedir.

Mevcut bir belgeyi [LoadFormat](../loadformat/) formatlarından herhangi birinde yüklemek için bir dosya adı veya akışı [Document](./) yapıcılarından birine gönderin. Boş bir belge oluşturmak için parametresiz yapıcıyı çağırın.

Belgeyi [SaveFormat](../saveformat/) formatlarından herhangi birinde kaydetmek için Save yöntemi aşırı yüklemelerinden birini kullanın.

Belge sayfalarını doğrudan bir **Graphics** nesnesine çizmek için [RenderToScale()](../) veya [RenderToSize()](../) yöntemini kullanın.

Belgeyi yazdırmak için [Print()](../) yöntemlerinden birini kullanın.

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

[Document](./) belgenin tüm diğer düğümlerini içeren bir ağacın kök düğümüdür. Ağaç bir Composite tasarım desenidir ve birçok açıdan XmlDocument'e benzer. Belgenin içeriği programlı olarak serbestçe manipüle edilebilir:

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



Belge ağacını programlı olarak oluşturma veya doldurma görevini basitleştiren [DocumentBuilder](../documentbuilder/) kullanmayı düşünün.

[Document](./) yalnızca [Section](../section/) nesnelerini içerebilir.

Microsoft Word'de geçerli bir belgenin en az bir bölümü olması gerekir.
## Ayrıca Bakınız

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
