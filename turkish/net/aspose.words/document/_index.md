---
title: Class Document
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Document sınıf. Bir Word belgesini temsil eder.
type: docs
weight: 420
url: /tr/net/aspose.words/document/
---
## Document class

Bir Word belgesini temsil eder.

```csharp
public class Document : DocumentBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Document](document/#constructor)() | Boş bir Word belgesi oluşturur. |
| [Document](document/#constructor_1)(Stream) | Bir akıştan var olan bir belgeyi açar. Dosya biçimini otomatik olarak algılar. |
| [Document](document/#constructor_3)(string) | Bir dosyadan var olan bir belgeyi açar. Dosya biçimini otomatik olarak algılar. |
| [Document](document/#constructor_2)(Stream, LoadOptions) | Bir akıştan var olan bir belgeyi açar. Şifreleme parolası gibi ek seçeneklerin belirlenmesine izin verir. |
| [Document](document/#constructor_4)(string, LoadOptions) | Bir dosyadan var olan bir belgeyi açar. Şifreleme parolası gibi ek seçeneklerin belirlenmesine izin verir. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Belgeye eklenen şablonun tam yolunu alır veya ayarlar. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Belge MS Word'de her açıldığında, belgedeki stillerin ekli şablondaki stiller ile eşleşecek şekilde güncellenip güncellenmediğini belirten bir bayrak alır veya ayarlar. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Belgenin arka plan şeklini alır veya ayarlar. null. olabilir |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Belgenin tüm yerleşik belge özelliklerini temsil eden bir koleksiyon döndürür. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Belge uyumluluğu seçeneklerine erişim sağlar (yani, ekranda girilen kullanıcı tercihleri). **uyumluluk** sekmesi **Seçenekler** Word'de iletişim kutusu). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca OOXML belgeleri için anlamlıdır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Belgenin tüm özel belge özelliklerini temsil eden bir koleksiyon döndürür. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Özel XML Veri Depolama Parçaları koleksiyonunu alır veya ayarlar. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Varsayılan sekme durakları arasındaki aralığı (nokta olarak) alır veya ayarlar. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Bu belge için dijital imzaların toplanmasını ve bunların doğrulama sonuçlarını alır. |
| override [Document](../../aspose.words/documentbase/document/) { get; } |  |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Bu belgedeki son notların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | **FieldOptions**belgede alan işlemeyi denetleme seçeneklerini temsil eden nesne. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk alt öğesini alır. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Belgedeki ilk bölümü alır. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Belge yazı tipi ayarlarını alır veya ayarlar. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Bu belgedeki dipnotların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Bir döndürür[`Frameset`](./frameset/)örneğin bu belge bir çerçeve sayfasını temsil ediyorsa. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Bu belge veya şablondaki sözlük belgesini alır veya ayarlar. Sözlük belgesi, bir belgede tanımlanan Otomatik Metin, Otomatik Düzeltme ve Yapı Taşı girdileri için bir depolama 'dir. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | İade **doğru** belge gramer açısından kontrol edilmişse. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | İade **doğru** belgede bir VBA projesi (makrolar) varsa. |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | İade **doğru** belgede izlenen değişiklikler varsa. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Belge tireleme seçeneklerine erişim sağlar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son alt öğesini alır. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Belgedeki son bölümü alır. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | **DüzenSeçenekleri** bu belgenin yerleşim sürecini denetleme seçeneklerini temsil eden nesne. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Belgede kullanılan liste formatına erişim sağlar. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Bir döndürür **Posta birleştirme** belge için adres mektup birleştirme işlevini temsil eden nesne. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Bir belge için tüm adres mektup birleştirme bilgilerini içeren nesneyi alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | İade **DüğümTürü.Belge** . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Belgenin orijinal dosya adını alır. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Bu nesneye yüklenen orijinal belgenin biçimini alır. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | "Bilinmeyen ilişkiler" kullanarak OOXML paketine bağlanan özel parçaların (keyfi içerik) koleksiyonunu alır veya ayarlar. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, aşağıdakilerin daha basit bir sürümüdür:[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | En son sayfa düzeni işlemi tarafından hesaplandığı şekliyle belgedeki sayfa sayısını alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Şu anda etkin olan belge koruma türünü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Belgeyi kaydettikten sonra Microsoft Word'ün yorumlardan, düzeltmelerden ve belge özelliklerinden tüm kullanıcı bilgilerini kaldıracağını belirten bir bayrak alır veya ayarlar. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Harici kaynakların nasıl yüklendiğini kontrol etmeye izin verir. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Bu belgede bulunan düzeltmelerin (izlenen değişiklikler) bir koleksiyonunu alır. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Bir belgenin orijinal mi yoksa gözden geçirilmiş sürümüyle mi çalışılacağını belirten bir değer alır veya ayarlar. |
| [Sections](../../aspose.words/document/sections/) { get; } | Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Form alanlarında gri gölgelemenin açılıp açılmayacağını belirtir. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Bu belgede dil bilgisi hatalarının görüntülenip görüntülenmeyeceğini belirtir. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Bu belgede yazım hatalarının görüntülenip görüntülenmeyeceğini belirtir. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | İade **doğru** belgenin yazım denetimi yapıldıysa. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Belgede tanımlanan stillerin bir koleksiyonunu döndürür. |
| [Theme](../../aspose.words/document/theme/) { get; } | [`Theme`](./theme/) bu belge için nesne. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | **Doğru** bu belge Microsoft Word'de düzenlendiğinde değişiklikler izleniyorsa. |
| [Variables](../../aspose.words/document/variables/) { get; } | Bir belgeye veya şablona eklenen değişkenler koleksiyonunu döndürür. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Alır veya ayarlar[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | DOC belgesinde depolanan belge sürümlerinin sayısını alır. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Belgenin Microsoft Word'de nasıl görüntüleneceğini denetleme seçenekleri sunar. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Verilerde veya biçimlendirme aslına uygunluk kaybına neden olabilecek bir sorun algılandığında çeşitli belge işleme prosedürleri sırasında çağrılır. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Belge filigranına erişim sağlar. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Görev bölmesi eklentilerinin listesini temsil eden bir koleksiyon döndürür. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Belge yazma koruması seçeneklerine erişim sağlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Belgede izlenen tüm değişiklikleri kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(Document, ImportFormatMode) | Belirtilen belgeyi bu belgenin sonuna ekler. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Belirtilen belgeyi bu belgenin sonuna ekler. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Belgedeki kullanılmayan stilleri ve listeleri temizler. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(CleanupOptions) | Verilenlere bağlı olarak kullanılmayan stilleri ve listeleri belgeden temizler[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | `Document` . |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [Compare](../../aspose.words/document/compare/#compare)(Document, string, DateTime) | Bu belgeyi, düzenleme ve biçim revizyonlarının sayısı olarak değişiklik üreten başka bir belgeyle karşılaştırır[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(Document, string, DateTime, CompareOptions) | Bu belgeyi, bir dizi düzenleme ve biçim revizyonu olarak değişiklikler üreten başka bir belgeyle karşılaştırır[`Revision`](../revision/) . Şunu kullanarak karşılaştırma seçeneklerini belirlemeye izin verir:[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(Document) | Stilleri belirtilen şablondan bir belgeye kopyalar. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(string) | Stilleri belirtilen şablondan bir belgeye kopyalar. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Belge bölüm içermiyorsa, tek paragraflı bir bölüm oluşturur. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Tablo stillerinde belirtilen biçimlendirmeyi, belgedeki tablolarda doğrudan biçimlendirmeye dönüştürür. |
| [ExtractPages](../../aspose.words/document/extractpages/)(int, int) | `Document` belirtilen sayfa aralığını temsil eden nesne. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(int) | Yazdırma veya oluşturma için yararlı olabilecek bir sayfayla ilgili sayfa boyutunu, yönünü ve diğer bilgileri alır. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool) | Bir düğümü başka bir belgeden geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool, ImportFormatMode) | Biçimlendirmeyi kontrol etme seçeneği ile bir düğümü başka bir belgeden geçerli belgeye aktarır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Belgenin tüm paragraflarında aynı biçimlendirmeyle çalıştırmaları birleştirir. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Alan türü değerlerini değiştirir[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) nın-nin[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) alan kodlarında yer alan alan türlerine karşılık gelecek şekilde belgenin tamamında. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Print](../../aspose.words/document/print/#print)() | Belgenin tamamını varsayılan yazıcıya yazdırır. |
| [Print](../../aspose.words/document/print/#print_1)(PrinterSettings) | Belgeyi belirtilen yazıcı ayarlarına göre yazdırır, standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak. |
| [Print](../../aspose.words/document/print/#print_3)(string) | Standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini kullanarak tüm belgeyi belirtilen yazıcıya yazdırın, . |
| [Print](../../aspose.words/document/print/#print_2)(PrinterSettings, string) | Belgeyi belirtilen yazıcı ayarlarına göre yazdırır, standart (Kullanıcı Arayüzü yok) yazdırma denetleyicisini ve bir belge adını kullanarak. |
| [Protect](../../aspose.words/document/protect/#protect)(ProtectionType) | Mevcut parolayı değiştirmeden veya rastgele bir parola atamadan belgeyi değişikliklerden korur. |
| [Protect](../../aspose.words/document/protect/#protect_1)(ProtectionType, string) | Belgeyi değişikliklerden korur ve isteğe bağlı olarak bir koruma parolası ayarlar. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Bu belgeden harici XML şeması referanslarını kaldırır. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Belgeden tüm makroları (VBA projesi) ve ayrıca araç çubuklarını ve komut özelleştirmelerini kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(int, Graphics, float, float, float) | Bir belge sayfasını birGraphics belirli bir ölçeğe nesne. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(int, Graphics, float, float, float, float) | Bir belge sayfasını birGraphics belirtilen bir boyuta nesne. |
| [Save](../../aspose.words/document/save/#save_2)(string) | Belgeyi bir dosyaya kaydeder. Uzantıdan kaydetme biçimini otomatik olarak belirler. |
| [Save](../../aspose.words/document/save/#save)(Stream, SaveFormat) | Belgeyi belirtilen biçimi kullanarak bir akışa kaydeder. |
| [Save](../../aspose.words/document/save/#save_1)(Stream, SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak belgeyi bir akışa kaydeder. |
| [Save](../../aspose.words/document/save/#save_3)(string, SaveFormat) | Belgeyi belirtilen biçimde bir dosyaya kaydeder. |
| [Save](../../aspose.words/document/save/#save_4)(string, SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak belgeyi bir dosyaya kaydeder. |
| [Save](../../aspose.words/document/save/#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | Belgeyi istemci tarayıcısına gönderir. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(string) | Belgede yaptığınız diğer tüm değişiklikleri, revizyon değişiklikleri olarak programlı olarak otomatik olarak işaretlemeye başlar. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(string, DateTime) | Belgede yaptığınız diğer tüm değişiklikleri, revizyon değişiklikleri olarak programlı olarak otomatik olarak işaretlemeye başlar. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Belge değişikliklerinin revizyon olarak otomatik olarak işaretlenmesini durdurur. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Belgenin tamamındaki alanların bağlantısını kaldırır. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Paroladan bağımsız olarak belgedeki korumayı kaldırır. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(string) | Doğru parola belirtilirse belgedeki korumayı kaldırır. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Belgenin tamamındaki alanların değerlerini günceller. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Belgedeki tüm liste öğeleri için liste etiketlerini günceller. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Belgenin sayfa düzenini yeniden oluşturur. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Güncellemeler[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) varsayılan seçenekleri kullanarak belgenin. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(ThumbnailGeneratingOptions) | Güncellemeler[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) belirtilen seçeneklere göre belgenin. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Belgenin sözcük sayısı özelliklerini günceller. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(bool) | Belgenin sözcük sayısı özelliklerini günceller, isteğe bağlı olarak günceller[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) özellik. |

### Notlar

bu **Belge** Aspose.Words kitaplığındaki merkezi bir nesnedir.

Mevcut bir belgeyi aşağıdakilerden herhangi birine yüklemek için[`LoadFormat`](../loadformat/) biçimlerinden birine bir dosya name veya bir akış iletin. **Belge** yapıcılar. Boş bir belge oluşturmak için, parametresiz the yapıcısını çağırın.

Belgeyi herhangi bir içine kaydetmek için Kaydet yöntemi aşırı yüklemelerinden birini kullanın.[`SaveFormat`](../saveformat/) biçimler.

Belge sayfalarını doğrudan bir **Grafikler** nesne kullanımı [`RenderToScale`](./rendertoscale/) veya[`RenderToSize`](./rendertosize/) yöntem.

Belgeyi yazdırmak için aşağıdakilerden birini kullanın:[`Print`](./print/)yöntemler.

[`MailMerge`](./mailmerge/) Microsoft Word'de tasarlanmış raporlarını çeşitli veri kaynaklarından gelen verilerle hızlı ve kolay bir şekilde doldurmaya olanak tanıyan Aspose.Words'ün raporlama motorudur. Veriler bir DataSet, DataTable, DataView, IDataReader veya bir dizi değerden olabilir.  **Posta birleştirme** veri kaynağında bulunan kayıtları gözden geçirecek ve bunları gerektiğinde büyüterek belgedeki adres mektup birleştirme alanlarına ekleyecektir.

**Belge** gibi belge çapındaki bilgileri depolar.[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) , listeler ve makrolar. Bu nesnelerin çoğuna, **Belge**.

bu **Belge**belgenin diğer tüm düğümlerini içeren bir ağacın kök düğümüdür. Ağaç bir Bileşik tasarım modelidir ve birçok yönden XmlDocument. 'ye benzer. Belgenin içeriği programlı olarak serbestçe değiştirilebilir:

* Belgenin düğümlerine, örneğin yazılan koleksiyonlar aracılığıyla erişilebilir.[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) vb.
* Belgenin düğümleri, düğüm türlerine göre kullanılarak seçilebilir.[`GetChildNodes`](../compositenode/getchildnodes/) veya bir XPath sorgusu kullanarak[`SelectNodes`](../compositenode/selectnodes/) veya[`SelectSingleNode`](../compositenode/selectsinglenode/).
* İçerik düğümleri, kullanılarak belgenin herhangi bir yerinden eklenebilir veya kaldırılabilir[`InsertBefore`](../compositenode/insertbefore/) ,[`InsertAfter`](../compositenode/insertafter/) , [`RemoveChild`](../compositenode/removechild/) ve temel sınıf tarafından sağlanan diğer yöntemleri[`CompositeNode`](../compositenode/).
* Her bir düğümün biçimlendirme öznitelikleri, o düğümün özellikleri aracılığıyla değiştirilebilir.

kullanmayı düşünün[`DocumentBuilder`](../documentbuilder/) bu, programlı olarak oluşturma veya belge ağacını doldurma görevini basitleştirir.

bu **Belge** sadece içerebilir[`Section`](../section/) nesneler.

Microsoft Word'de geçerli bir belgenin en az bir bölümü olmalıdır.

### Örnekler

DataTable'daki verilerle adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres mektup birleştirme için veri kaynağı olarak bir DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablodaki her satır için bir çıktı adres mektup birleştirme belgesi oluşturmak üzere adres mektup birleştirme için tüm tabloyu kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres mektup birleştirme kaynak belgesi oluşturur.
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


