---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: Sorunsuz Word belge düzenlemesi için Aspose.Words.Document sınıfını keşfedin. Projelerinizi güçlü özellikler ve kolay entegrasyonla geliştirin.
type: docs
weight: 640
url: /tr/net/aspose.words/document/
---
## Document class

Bir Word belgesini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgeyle Çalışma](https://docs.aspose.com/words/net/working-with-document/) belgeleme makalesi.

```csharp
public class Document : DocumentBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Document](document/#constructor)() | Boş bir Word belgesi oluşturur. |
| [Document](document/#constructor_1)(*Stream*) | Bir akıştan mevcut bir belgeyi açar. Dosya biçimini otomatik olarak algılar. |
| [Document](document/#constructor_3)(*string*) | Bir dosyadan mevcut bir belgeyi açar. Dosya biçimini otomatik olarak algılar. |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Bir akıştan mevcut bir belgeyi açar. Şifreleme parolası gibi ek seçeneklerin belirtilmesine olanak tanır. |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Bir dosyadan mevcut bir belgeyi açar. Şifreleme parolası gibi ek seçeneklerin belirtilmesine olanak tanır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Belgeye eklenen şablonun tam yolunu alır veya ayarlar. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Belgedeki stillerin, belge MS Word'de her açıldığında ekli şablondaki stillerle eşleşecek şekilde güncellenip güncellenmeyeceğini belirten bir bayrak alır veya ayarlar. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Belgenin arka plan şeklini alır veya ayarlar.`hükümsüz` . |
| [Bibliography](../../aspose.words/document/bibliography/) { get; } | Şunu alır:[`Bibliography`](./bibliography/)belgede mevcut kaynakların listesini temsil eden nesne. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Belgenin tüm yerleşik belge özelliklerini temsil eden bir koleksiyon döndürür. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Belge uyumluluk seçeneklerine erişim sağlar (yani, belgeye girilen kullanıcı tercihleri)**Uyumluluk** sekmesi**Seçenekler**Word'de iletişim kutusu). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca OOXML belgeleri için mantıklıdır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Belgenin tüm özel belge özelliklerini temsil eden bir koleksiyon döndürür. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Özel XML Veri Depolama Parçaları koleksiyonunu alır veya ayarlar. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Varsayılan sekme durakları arasındaki aralığı (nokta cinsinden) alır veya ayarlar. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Bu belge için dijital imzaların koleksiyonunu ve bunların doğrulama sonuçlarını alır. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Bu örneği alır. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Bu belgedeki dipnotların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sağlar. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Bir tane alır[`FieldOptions`](../../aspose.words.fields/fieldoptions/) belgedeki alan işlemeyi kontrol etme seçeneklerini temsil eden nesne. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Belgedeki ilk bölümü alır. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Belge yazı tipi ayarlarını alır veya ayarlar. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Bu belgedeki dipnotların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sağlar. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Belgede tanımlanan dipnot/sonnot ayırıcılarına erişim sağlar. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Bir[`Frameset`](./frameset/) örneğin bu belge bir çerçeve sayfasını temsil ediyorsa. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Bu belge veya şablon içindeki sözlük belgesini alır veya ayarlar. Sözlük belgesi, bir belgede tanımlanan Otomatik Metin, Otomatik Düzeltme ve Yapı Taşı girişleri için bir depolama 'dir. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Geri Döndürür`doğru` belgenin dil bilgisi açısından kontrol edilip edilmediği. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Geri Döndürür`doğru` eğer belgenin bir VBA projesi varsa (makrolar). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Geri Döndürür`doğru` belgede izlenen değişiklikler varsa. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Belge tireleme seçeneklerine erişim sağlar. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Kelime sayısı istatistiklerine metin kutuları, dipnotlar ve son notların dahil edilip edilmeyeceğini belirtir. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Bir belgenin karakter aralığı ayarını alır veya ayarlar. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Belgedeki son bölümü alır. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Bir tane alır[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) Bu belgenin düzen sürecini kontrol etmek için seçenekleri temsil eden nesne. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Belgede kullanılan liste biçimlendirmesine erişim sağlar. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Bir[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) belge için posta birleştirme işlevini temsil eden nesne. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Bir belgenin tüm posta birleştirme bilgilerini içeren nesneyi alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | Geri DöndürürDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Belgenin orijinal dosya adını alır. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Bu nesneye yüklenen orijinal belgenin biçimini alır. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | "Bilinmeyen ilişkiler" kullanılarak OOXML paketine bağlı olan özel parçaların (keyfi içerik) koleksiyonunu alır veya ayarlar. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, daha basit bir sürümüdür[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | En son sayfa düzeni işlemi tarafından hesaplanan belgedeki sayfa sayısını alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Şu anda etkin olan belge koruma türünü alır. |
| [PunctuationKerning](../../aspose.words/document/punctuationkerning/) { get; set; } | Harfin hem Latin metinlerine hem de noktalama işaretlerine uygulanıp uygulanmayacağını belirtir. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Microsoft Word'ün belgeyi kaydederken tüm kullanıcı bilgilerini yorumlardan, düzeltmelerden ve belge özelliklerinden kaldıracağını belirten bir bayrak alır veya ayarlar. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Harici kaynakların nasıl yükleneceğini kontrol etmenizi sağlar. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Bu belgede bulunan revizyonların (izlenen değişikliklerin) bir koleksiyonunu alır. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Bir belgenin orijinal veya revize edilmiş sürümüyle çalışılıp çalışılmayacağını belirten bir değer alır veya ayarlar. |
| [Sections](../../aspose.words/document/sections/) { get; } | Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Form alanlarında gri gölgelendirmenin açılıp açılmayacağını belirtir. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Bu belgede dilbilgisi hatalarının gösterilip gösterilmeyeceğini belirtir. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Bu belgede yazım hatalarının gösterilip gösterilmeyeceğini belirtir. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Geri Döndürür`doğru` belgenin yazım denetimi yapılmışsa. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Belgede tanımlanan stil koleksiyonunu döndürür. |
| [Theme](../../aspose.words/document/theme/) { get; } | Şunu alır:[`Theme`](./theme/) bu belge için nesne. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | Bu belge Microsoft Word'de düzenlendiğinde değişiklikler izleniyorsa doğrudur. |
| [Variables](../../aspose.words/document/variables/) { get; } | Bir belgeye veya şablona eklenen değişken koleksiyonunu döndürür. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Bir değeri alır veya ayarlar[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | DOC belgesinde saklanan belge sürümlerinin sayısını alır. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Belgenin Microsoft Word'de nasıl görüntüleneceğini kontrol etmek için seçenekler sağlar. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Çeşitli belge işleme prosedürleri sırasında, veri veya biçimlendirme sadakat kaybına neden olabilecek bir sorun algılandığında çağrılır. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Belge filigranına erişim sağlar. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Görev bölmesi eklentilerinin bir listesini temsil eden bir koleksiyon döndürür. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Belge yazma koruması seçeneklerine erişim sağlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Belgedeki tüm izlenen değişiklikleri kabul eder. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Belgenin sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Belgenin başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | Belirtilen belgeyi bu belgenin sonuna ekler. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Belirtilen belgeyi bu belgenin sonuna ekler. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Belgeden kullanılmayan stilleri ve listeleri temizler. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | Belirtilenlere bağlı olarak kullanılmayan stilleri ve listeleri belgeden temizler[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Derin bir kopyasını gerçekleştirir`Document` . |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | Bu belgeyi düzenleme ve biçim revizyonlarının sayısı olarak değişiklik üreten başka bir belgeyle karşılaştırır[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Bu belgeyi başka bir belgeyle karşılaştırır ve bir dizi düzenleme ve biçim revizyonu olarak değişiklikler üretir[`Revision`](../revision/) . Karşılaştırma seçeneklerini belirtmeye olanak tanır[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | Belirtilen şablondan bir belgeye stilleri kopyalar. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | Belirtilen şablondan bir belgeye stilleri kopyalar. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Belgede bölüm yoksa, bir paragraf içeren bir bölüm oluşturur. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Tablo stillerinde belirtilen biçimlendirmeyi, belgedeki tablolarda doğrudan biçimlendirmeye dönüştürür. |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | şunu döndürür:`Document` belirtilen sayfa aralığını temsil eden nesne. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | Yazdırma veya işleme için yararlı olabilecek bir sayfa hakkında sayfa boyutu, yönlendirme ve diğer bilgileri alır. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | Başka bir belgeden bir düğümü geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Biçimlendirmeyi kontrol etme seçeneğiyle başka bir belgeden geçerli belgeye bir düğüm aktarır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Belgenin tüm paragraflarında aynı biçimlendirmeyle çalışmaları birleştirir. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Alan türü değerlerini değiştirir[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) ile ilgili[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) tüm belgede, alan kodlarında bulunan alan türlerine karşılık gelecek şekilde. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Print](../../aspose.words/document/print/#print)() | Tüm belgeyi varsayılan yazıcıya yazdırır. |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | Belgeyi belirtilen yazıcı ayarlarına göre yazdırır, standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak. |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | Tüm belgeyi belirtilen yazıcıya yazdırın, standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak. |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | Standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini ve bir belge adını kullanarak, belirtilen yazıcı ayarlarına göre belgeyi yazdırır. |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | Mevcut parolayı değiştirmeden belgeyi değişikliklere karşı korur veya rastgele bir parola atar. |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | Belgeyi değişikliklere karşı korur ve isteğe bağlı olarak bir koruma parolası ayarlar. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveBlankPages](../../aspose.words/document/removeblankpages/)() | Belgeden boş sayfaları kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Belirtilen alt düğümü kaldırır. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Bu belgeden harici XML şema referanslarını kaldırır. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Belgeden tüm makroları (VBA projesi) ve araç çubuklarını ve komut özelleştirmelerini kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | Bir belge sayfasını birGraphics belirli bir ölçeğe göre nesne. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | Bir belge sayfasını birGraphics nesneyi belirtilen bir boyuta taşı. |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | Belgeyi bir dosyaya kaydeder. Uzantıdan kaydetme biçimini otomatik olarak belirler. |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | Belgeyi belirtilen biçimi kullanarak bir akışa kaydeder. |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak belgeyi bir akışa kaydeder. |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | Belgeyi belirtilen biçimde bir dosyaya kaydeder. |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak belgeyi bir dosyaya kaydeder. |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belgeyi istemci tarayıcısına gönderir. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../node/) XPath ifadesiyle eşleşen. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | Belgede yaptığınız tüm sonraki değişiklikleri programatik olarak revizyon değişiklikleri olarak otomatik olarak işaretlemeye başlar. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | Belgede yaptığınız tüm sonraki değişiklikleri programatik olarak revizyon değişiklikleri olarak otomatik olarak işaretlemeye başlar. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Belge değişikliklerinin revizyon olarak otomatik olarak işaretlenmesini durdurur. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Tüm belgedeki alanların bağlantısını kaldırır. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Paroladan bağımsız olarak belgenin korumasını kaldırır. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | Doğru bir parola belirtilirse belgeden korumayı kaldırır. |
| [UpdateActualReferenceMarks](../../aspose.words/document/updateactualreferencemarks/)() | Günceller[`ActualReferenceMark`](../../aspose.words.notes/footnote/actualreferencemark/) belgedeki tüm dipnot ve sonnotların mülkiyeti. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Tüm belgedeki alanların değerlerini günceller. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Belgedeki tüm liste öğelerinin liste etiketlerini günceller. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Belgenin sayfa düzenini yeniden oluşturur. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Güncellemeler[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) varsayılan seçenekleri kullanarak belgenin. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | Güncellemeler[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) Belirtilen seçeneklere göre belgenin. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Belgenin kelime sayısı özelliklerini günceller. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | Belgenin kelime sayısı özelliklerini günceller, isteğe bağlı olarak günceller[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) mülk. |

## Notlar

The`Document` Aspose.Words kütüphanesinin merkezi nesnesidir.

Mevcut bir belgeyi herhangi birine yüklemek için[`LoadFormat`](../loadformat/) biçimleri, dosya adı veya bir akışı bunlardan birine geçirin`Document` yapıcılar. Boş bir belge oluşturmak için, parametresiz the yapıcısını çağırın.

Belgeyi herhangi bir dosyasına kaydetmek için Kaydet yöntemi aşırı yüklemelerinden birini kullanın[`SaveFormat`](../saveformat/) biçimleri.

Belge sayfalarını doğrudan bir belgeye çizmek için**Grafikler** nesne use [`RenderToScale`](./rendertoscale/) veya[`RenderToSize`](./rendertosize/) yöntem.

Belgeyi yazdırmak için aşağıdakilerden birini kullanın:[`Print`](./print/) Yöntemler.

[`MailMerge`](./mailmerge/)Microsoft Word'de tasarlanmış raporları çeşitli veri kaynaklarından gelen verilerle hızlı ve kolay bir şekilde doldurmanıza olanak sağlayan Aspose.Words'ün raporlama motorudur. Veriler bir DataSet, DataTable, DataView, IDataReader veya bir dizi değerden olabilir. **Posta birleştirme** Veri kaynağında bulunan kayıtları inceleyecek ve bunları gerektiği gibi genişleterek belgedeki birleştirme alanlarına ekleyecektir.

`Document` belge genelindeki bilgileri depolar, örneğin[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) , listeler ve makrolar. Bu nesnelerin çoğuna, ilgili özellikler aracılığıyla erişilebilir.`Document`.

The`Document` belgenin diğer tüm düğümlerini içeren bir ağacın kök düğümüdür. Ağaç bir Bileşik tasarım desenidir ve birçok yönden XmlDocument'a benzer. Belgenin içeriği programatik olarak serbestçe değiştirilebilir:

* Belgenin düğümlerine, örneğin yazılmış koleksiyonlar aracılığıyla erişilebilir[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) vesaire.
* Belgenin düğümleri, düğüm türlerine göre kullanılarak seçilebilir.[`GetChildNodes`](../compositenode/getchildnodes/) veya bir XPath sorgusu kullanarak[`SelectNodes`](../compositenode/selectnodes/) veya[`SelectSingleNode`](../compositenode/selectsinglenode/).
* İçerik düğümleri, belgenin herhangi bir yerinden kullanılarak eklenebilir veya kaldırılabilir[`InsertBefore`](../compositenode/insertbefore/) ,[`InsertAfter`](../compositenode/insertafter/) , [`RemoveChild`](../compositenode/removechild/) ve temel sınıf tarafından sağlanan other yöntemleri[`CompositeNode`](../compositenode/).
* Her düğümün biçimlendirme nitelikleri, o düğümün özellikleri aracılığıyla değiştirilebilir.

Kullanmayı düşünün[`DocumentBuilder`](../documentbuilder/) Bu, programlı olarak creation veya belge ağacını doldurma görevini basitleştirir.

The`Document` sadece içerebilir[`Section`](../section/) nesneler.

Microsoft Word'de geçerli bir belgenin en az bir bölümü olması gerekir.

## Örnekler

DataTable'daki verilerle posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda bir posta birleştirme için veri kaynağı olarak DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablonun tamamını kullanarak, tablodaki her satır için tek bir çıktı birleştirme belgesi oluşturun:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Tablonun bir satırını kullanarak tek bir çıktı birleştirme belgesi oluşturun:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Bir posta birleştirme kaynak belgesi oluşturur.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Ayrıca bakınız

* class [DocumentBase](../documentbase/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
