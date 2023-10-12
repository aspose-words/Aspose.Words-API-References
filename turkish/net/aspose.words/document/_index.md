---
title: Class Document
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Document sınıf. Bir Word belgesini temsil eder.
type: docs
weight: 430
url: /tr/net/aspose.words/document/
---
## Document class

Bir Word belgesini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgeyle Çalışmak](https://docs.aspose.com/words/net/working-with-document/) dokümantasyon makalesi.

```csharp
public class Document : DocumentBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Document](document/#constructor)() | Boş bir Word belgesi oluşturur. |
| [Document](document/#constructor_1)(Stream) | Bir akıştan mevcut bir belgeyi açar. Dosya biçimini otomatik olarak algılar. |
| [Document](document/#constructor_3)(string) | Bir dosyadan mevcut bir belgeyi açar. Dosya biçimini otomatik olarak algılar. |
| [Document](document/#constructor_2)(Stream, LoadOptions) | Bir akıştan mevcut bir belgeyi açar. Şifreleme şifresi gibi ek seçeneklerin belirtilmesine olanak tanır. |
| [Document](document/#constructor_4)(string, LoadOptions) | Bir dosyadan mevcut bir belgeyi açar. Şifreleme şifresi gibi ek seçeneklerin belirtilmesine olanak tanır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Belgeye eklenen şablonun tam yolunu alır veya ayarlar. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Belgedeki stillerin, belge MS Word'de her açıldığında ekli şablondaki stilleriyle eşleşecek şekilde güncellenip güncellenmediğini belirten bir bayrak alır veya ayarlar. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Belgenin arka plan şeklini alır veya ayarlar. Olabilir`hükümsüz` . |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Belgenin tüm yerleşik belge özelliklerini temsil eden bir koleksiyon döndürür. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Belge uyumluluk seçeneklerine (yani, **Uyumluluk** sekmesi **Seçenekler** Word'deki iletişim kutusu). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca OOXML belgeleri için anlamlıdır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Belgenin tüm özel belge özelliklerini temsil eden bir koleksiyon döndürür. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Özel XML Veri Depolama Parçalarının koleksiyonunu alır veya ayarlar. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Varsayılan sekme durakları arasındaki aralığı (puan cinsinden) alır veya ayarlar. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Bu belge için dijital imzaların toplanmasını ve doğrulama sonuçlarını alır. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Bu örneği alır. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Bu belgedeki son notların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Bir alır[`FieldOptions`](../../aspose.words.fields/fieldoptions/) belgedeki alan işlemeyi kontrol etme seçeneklerini temsil eden nesne. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Belgedeki ilk bölümü alır. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Belge yazı tipi ayarlarını alır veya ayarlar. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Bu belgedeki dipnotların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Bir değeri döndürür[`Frameset`](./frameset/)örneğin bu belge bir çerçeve sayfasını temsil ediyorsa. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Bu belge veya şablon içindeki sözlük belgesini alır veya ayarlar. Sözlük belgesi, bir belgede tanımlanan Otomatik Metin, Otomatik Düzeltme ve Yapı Taşı girişleri için bir depolama 'dir. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | İadeler`doğru` belge dilbilgisi açısından kontrol edilmişse. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | İadeler`doğru` bu düğümün herhangi bir alt düğümü varsa. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | İadeler`doğru` belgede bir VBA projesi (makrolar) varsa. |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | İadeler`doğru` belgede izlenen herhangi bir değişiklik varsa. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Belge tireleme seçeneklerine erişim sağlar. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Kelime sayısı istatistiklerine metin kutularının, dipnotların ve son notların dahil edilip edilmeyeceğini belirtir. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | İadeler`doğru` çünkü bu düğüm alt düğümlere sahip olabilir. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Bir belgenin karakter aralığı ayarını alır veya ayarlar. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Belgedeki son bölümü alır. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Bir alır[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) bu belgenin düzen sürecini kontrol etme seçeneklerini temsil eden nesne. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Belgede kullanılan liste formatına erişim sağlar. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Bir değeri döndürür[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) belgenin adres-mektup birleştirme işlevini temsil eden nesne. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Bir belgeye ilişkin tüm adres-mektup birleştirme bilgilerini içeren nesneyi alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | İadelerDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Belgenin orijinal dosya adını alır. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Bu nesneye yüklenen orijinal belgenin biçimini alır. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | "Bilinmeyen ilişkiler" kullanılarak OOXML paketine bağlanan özel parçaların (rastgele içerik) koleksiyonunu alır veya ayarlar. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, daha basit bir versiyonudur[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | En son sayfa düzeni işlemiyle hesaplanan belgedeki sayfa sayısını alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Şu anda etkin olan belge koruma türünü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Belgeyi kaydettikten sonra Microsoft Word'ün yorumlardan, düzeltmelerden ve belge özelliklerinden tüm kullanıcı bilgilerini kaldıracağını belirten bir işaret alır veya ayarlar. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Harici kaynakların nasıl yüklendiğini kontrol etmeye izin verir. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Bu belgede mevcut olan revizyonların (izlenen değişiklikler) bir koleksiyonunu alır. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Bir belgenin orijinal sürümüyle mi yoksa revize edilmiş sürümüyle mi çalışılacağını belirten bir değer alır veya ayarlar. |
| [Sections](../../aspose.words/document/sections/) { get; } | Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Form alanlarında gri gölgelemenin açılıp açılmayacağını belirtir. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Bu belgede dilbilgisi hatalarının görüntülenip görüntülenmeyeceğini belirtir. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Bu belgede yazım hatalarının görüntülenip görüntülenmeyeceğini belirtir. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | İadeler`doğru` belgenin yazım denetimi yapılmışsa. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Belgede tanımlanan stillerin bir koleksiyonunu döndürür. |
| [Theme](../../aspose.words/document/theme/) { get; } | Alır[`Theme`](./theme/) bu belgeye ait nesne. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | Bu belge Microsoft Word'de düzenlenirken değişiklikler izleniyorsa doğrudur. |
| [Variables](../../aspose.words/document/variables/) { get; } | Bir belgeye veya şablona eklenen değişkenlerin koleksiyonunu döndürür. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Bir değeri alır veya ayarlar[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | DOC belgesinde saklanan belge sürümlerinin sayısını alır. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Belgenin Microsoft Word'de nasıl görüntüleneceğini kontrol etmek için seçenekler sunar. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Çeşitli belge işleme prosedürleri sırasında, verilerde veya formatta uygunluk kaybıyla sonuçlanabilecek bir sorun algılandığında çağrılır. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Belge filigranına erişim sağlar. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Görev bölmesi eklentilerinin listesini temsil eden bir koleksiyon döndürür. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Belge yazma koruması seçeneklerine erişim sağlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(DocumentVisitor) | Ziyaretçi kabul eder. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Belgede izlenen tüm değişiklikleri kabul eder. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(Document, ImportFormatMode) | Belirtilen belgeyi bu belgenin sonuna ekler. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Belirtilen belgeyi bu belgenin sonuna ekler. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Belgedeki kullanılmayan stilleri ve listeleri temizler. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(CleanupOptions) | Verilenlere bağlı olarak kullanılmayan stilleri ve listeleri belgeden temizler.[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Derin bir kopyasını gerçekleştirir.`Document` . |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [Compare](../../aspose.words/document/compare/#compare)(Document, string, DateTime) | Bu belgeyi, düzenleme ve biçim revizyonlarının sayısı olarak değişiklik üreten başka bir belgeyle karşılaştırır[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(Document, string, DateTime, CompareOptions) | Bu belgeyi, bir dizi düzenleme ve biçim revizyonu şeklinde değişiklik üreten başka bir belgeyle karşılaştırır[`Revision`](../revision/) . Karşılaştırma seçeneklerini belirtmeye olanak sağlar.[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(Document) | Stilleri belirtilen şablondan bir belgeye kopyalar. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(string) | Stilleri belirtilen şablondan bir belgeye kopyalar. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Belgede bölüm yoksa, tek paragraflı bir bölüm oluşturur. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Tablo stillerinde belirtilen biçimlendirmeyi, belgedeki tablolardaki doğrudan biçimlendirmeye dönüştürür. |
| [ExtractPages](../../aspose.words/document/extractpages/)(int, int) | Şunu döndürür:`Document` belirtilen sayfa aralığını temsil eden nesne. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atayı alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(int) | Yazdırma veya işleme için faydalı olabilecek sayfa boyutunu, yönünü ve bir sayfa hakkındaki diğer bilgileri alır. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool) | Başka bir belgedeki bir düğümü geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool, ImportFormatMode) | Biçimlendirmeyi kontrol etme seçeneğiyle birlikte başka bir belgedeki bir düğümü geçerli belgeye aktarır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisinde belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Birleştirmeler belgenin tüm paragraflarında aynı formatta çalışır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Alan türü değerlerini değiştirir[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) ile ilgili[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) alan kodlarında yer alan alan türlerine karşılık gelecek şekilde tüm belgede. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Print](../../aspose.words/document/print/#print)() | Belgenin tamamını varsayılan yazıcıya yazdırır. |
| [Print](../../aspose.words/document/print/#print_1)(PrinterSettings) | Belgeyi belirtilen yazıcı ayarlarına göre standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak yazdırır. |
| [Print](../../aspose.words/document/print/#print_3)(string) | Standart (Kullanıcı Arayüzü olmayan) yazdırma denetleyicisini kullanarak belgenin tamamını belirtilen yazıcıya, yazdırın. |
| [Print](../../aspose.words/document/print/#print_2)(PrinterSettings, string) | Belgeyi belirtilen yazıcı ayarlarına göre standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini ve belge adını kullanarak yazdırır. |
| [Protect](../../aspose.words/document/protect/#protect)(ProtectionType) | Mevcut şifreyi değiştirmeden belgeyi değişikliklere karşı korur veya rastgele bir şifre atar. |
| [Protect](../../aspose.words/document/protect/#protect_1)(ProtectionType, string) | Belgeyi değişikliklere karşı korur ve isteğe bağlı olarak bir koruma parolası ayarlar. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Bu belgeden harici XML şeması referanslarını kaldırır. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Tüm makroların (VBA projesinin) yanı sıra araç çubuklarını ve komut özelleştirmelerini belgeden kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/)Geçerli düğümün alt düğümleri. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(int, Graphics, float, float, float) | Bir belge sayfasını birGraphics belirtilen ölçeğe itiraz. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(int, Graphics, float, float, float, float) | Bir belge sayfasını birGraphics belirtilen boyuta nesne. |
| [Save](../../aspose.words/document/save/#save_2)(string) | Belgeyi bir dosyaya kaydeder. Uzantıdan kaydetme biçimini otomatik olarak belirler. |
| [Save](../../aspose.words/document/save/#save)(Stream, SaveFormat) | Belirtilen formatı kullanarak belgeyi bir akışa kaydeder. |
| [Save](../../aspose.words/document/save/#save_1)(Stream, SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak belgeyi bir akışa kaydeder. |
| [Save](../../aspose.words/document/save/#save_3)(string, SaveFormat) | Belgeyi belirtilen formatta bir dosyaya kaydeder. |
| [Save](../../aspose.words/document/save/#save_4)(string, SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak belgeyi bir dosyaya kaydeder. |
| [Save](../../aspose.words/document/save/#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | Belgeyi istemci tarayıcısına gönderir. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | İlkini seçer[`Node`](../node/) XPath ifadesiyle eşleşen. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(string) | Belgede yaptığınız diğer tüm değişiklikleri otomatik olarak revizyon değişiklikleri olarak işaretlemeye başlar. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(string, DateTime) | Belgede yaptığınız diğer tüm değişiklikleri otomatik olarak revizyon değişiklikleri olarak işaretlemeye başlar. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Belge değişikliklerinin otomatik olarak revizyon olarak işaretlenmesini durdurur. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Tüm belgedeki alanların bağlantısını kaldırır. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Paroladan bağımsız olarak belgedeki korumayı kaldırır. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(string) | Doğru parola belirtilirse belgedeki korumayı kaldırır. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Belgenin tamamındaki alanların değerlerini günceller. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Belgedeki tüm liste öğeleri için liste etiketlerini günceller. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Belgenin sayfa düzenini yeniden oluşturur. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Güncellemeler[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) varsayılan seçenekleri kullanarak belgenin. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(ThumbnailGeneratingOptions) | Güncellemeler[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) belirtilen seçeneklere göre belgenin. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Belgenin kelime sayısı özelliklerini günceller. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(bool) | Belgenin kelime sayısı özelliklerini günceller, isteğe bağlı olarak günceller[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) özellik. |

### Notlar

`Document` Aspose.Words kütüphanesindeki merkezi bir nesnedir.

Mevcut bir belgeyi herhangi bir yere yüklemek için[`LoadFormat`](../loadformat/) formatlarından birine bir dosya name veya bir akış iletin.`Document`inşaatçılar. Boş bir belge oluşturmak için the yapıcısını parametreler olmadan çağırın.

Belgeyi the 'den herhangi birine kaydetmek için Save yöntemi aşırı yüklemelerinden birini kullanın.[`SaveFormat`](../saveformat/) formatlar.

Belge sayfalarını doğrudan bir sayfaya çizmek için **Grafik** nesne kullanımı [`RenderToScale`](./rendertoscale/) veya[`RenderToSize`](./rendertosize/) yöntem.

Belgeyi yazdırmak için aşağıdakilerden birini kullanın:[`Print`](./print/) yöntemler.

[`MailMerge`](./mailmerge/) Aspose.Words'ün Microsoft Word'de tasarlanmış raporların çeşitli veri kaynaklarından gelen verilerle hızlı ve kolay bir şekilde doldurulmasına olanak sağlayan raporlama motorudur. Veriler bir DataSet, DataTable, DataView, IDataReader veya bir değer dizisinden olabilir.  **Posta birleştirme** veri kaynağında bulunan kayıtları inceleyecek ve bunları gerektiği gibi büyüterek belgedeki adres-mektup birleştirme alanlarına ekleyecektir.

`Document` gibi belge genelindeki bilgileri saklar[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) listeler ve makrolar. Bu nesnelerin çoğuna, ilgili nesnenin ilgili özellikleri aracılığıyla erişilebilir.`Document`.

`Document` belgenin tüm diğer düğümlerini içeren bir ağacın kök düğümüdür. Ağaç bir Bileşik tasarım desenidir ve birçok yönden XmlDocument'e benzer. Belgenin içeriği program aracılığıyla serbestçe değiştirilebilir:

* Belgenin düğümlerine, örneğin yazılan koleksiyonlar aracılığıyla erişilebilir.[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) vesaire.
* Belgenin düğümleri, kullanılarak düğüm türlerine göre seçilebilir[`GetChildNodes`](../compositenode/getchildnodes/) veya bir XPath sorgusu kullanarak[`SelectNodes`](../compositenode/selectnodes/) veya[`SelectSingleNode`](../compositenode/selectsinglenode/).
* İçerik düğümleri, kullanılarak belgenin herhangi bir yerinden eklenebilir veya kaldırılabilirNode) ,Node) , Node) ve temel sınıf tarafından sağlanan other yöntemleri[`CompositeNode`](../compositenode/).
* Her düğümün biçimlendirme öznitelikleri, o düğümün özellikleri aracılığıyla değiştirilebilir.

Kullanmayı düşünün[`DocumentBuilder`](../documentbuilder/)bu, programlı olarak oluşturma veya belge ağacını doldurma görevini basitleştirir.

`Document` yalnızca içerebilir[`Section`](../section/) nesneler.

Microsoft Word'de geçerli bir belgenin en az bir bölümü olması gerekir.

### Örnekler

DataTable'daki verilerle adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres-mektup birleştirme için veri kaynağı olarak DataTable'ı kullanmanın iki yolu verilmiştir.
    // 1 - Tablodaki her satır için bir çıktı adres-mektup birleştirme belgesi oluşturmak amacıyla adres-mektup birleştirme için tablonun tamamını kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres-mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres-mektup birleştirme kaynak belgesi oluşturur.
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


