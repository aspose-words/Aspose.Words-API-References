---
title: StructuredDocumentTag
second_title: Aspose.Words for .NET API Referansı
description: Bir belgedeki yapılandırılmış bir belge etiketini SDT veya içerik denetimi temsil eder.
type: docs
weight: 3820
url: /tr/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Bir belgedeki yapılandırılmış bir belge etiketini (SDT veya içerik denetimi) temsil eder.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag)(DocumentBase, SdtType, MarkupLevel) | Yeni bir örneğini başlatır **Yapılandırılmış belge etiketi** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance) { get; set; } | Yapılandırılmış bir belge etiketinin görünümünü alır/ayarlar. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory) { get; set; } | Bunun için yapı taşı kategorisini belirtir **SDT** node. null olamaz. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery) { get; set; } | Bunun için yapı taşı türünü belirtir **SDT** . Boş olamaz. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype) { get; set; } | Bunun için takvim türünü belirtir **SDT** . VarsayılanDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked) { get; set; } | Onay Kutusunun geçerli durumunu alır/ayarlar **SDT** . Bu özellik için varsayılan değer false'tur. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Color](../../aspose.words.markup/structureddocumenttag/color) { get; set; } | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont) { get; } | Girilen metne uygulanacak yazı tipi biçimlendirmesi **SDT** . |
| [Count](../../aspose.words/compositenode/count) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat) { get; set; } | Tarihlerin görüntülendiği biçimi temsil eden dize. Boş olamaz. İngilizce (ABD) için tarihler "aa/gg/yyyy" şeklindedir. |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale) { get; set; } | Burada görüntülenen tarih için dil biçimini ayarlamaya/almaya izin verir. **SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat) { get; set; } | Bir tarih SDT'sinin saklandığı tarihin biçimini alır/ayarlar. **SDT** belgenin veri deposundaki bir XML düğümüne bağlıdır. Varsayılan değerDateTime |
| virtual [Document](../../aspose.words/node/document) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont) { get; } | Girilen metnin son karakterine uygulanacak yazı tipi biçimlendirmesi **SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Düğümün ilk alt öğesini alır. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate) { get; set; } | Buna en son girilen tam tarih ve saati belirtir **SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| [Id](../../aspose.words.markup/structureddocumenttag/id) { get; } | Bunun için benzersiz bir salt okunur kalıcı sayısal kimlik belirtir **SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext) { get; set; } | Bunun içeriğinin olup olmadığını belirtir. **SDT** yer tutucu text içerecek şekilde yorumlanmalıdır (SDT içindeki normal metin içeriklerinin aksine). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary) { get; set; } | Bunun olup olmadığını belirtir **SDT** content değiştirildiğinde WordProcessingML belgesinden kaldırılacaktır. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Düğümün son alt öğesini alır. |
| [Level](../../aspose.words.markup/structureddocumenttag/level) { get; } | Bunun hangi düzeyde olduğunu alır **SDT** belge ağacında gerçekleşir. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems) { get; } | Alır[`SdtListItemCollection`](../sdtlistitemcollection) bununla ilişkili **SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol) { get; set; } | true olarak ayarlandığında, bu özellik bir kullanıcının bunu silmesini engeller. **SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents) { get; set; } | true olarak ayarlandığında, bu özellik bir kullanıcının bunun içeriğini düzenlemesini engeller. **SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline) { get; set; } | Bunun olup olmadığını belirtir **SDT** birden çok metin satırına izin verir. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype) { get; } | İade **NodeType.StructuredDocumentTag** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder) { get; } | [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) bu SDT çalıştırma içeriği boş olduğunda görüntülenmesi gereken yer tutucu metni içeren, ilişkili eşlenen XML öğesi,[`XmlMapping`](./xmlmapping) element veya[`IsShowingPlaceholderText`](./isshowingplaceholdertext) eleman doğrudur. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername) { get; set; } | Adını alır veya ayarlar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) yer tutucu metni içeren. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype) { get; } | Bunun türünü alır **Yapılandırılmış belge etiketi** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style) { get; set; } | Yapılandırılmış belge etiketinin Stilini alır veya ayarlar. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename) { get; set; } | Yapılandırılmış belge etiketine uygulanan stilin adını alır veya ayarlar. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag) { get; set; } | Geçerli SDT düğümüyle ilişkili bir etiketi belirtir. Boş olamaz. |
| [Title](../../aspose.words.markup/structureddocumenttag/title) { get; set; } | Bununla ilişkili kolay adı belirtir **SDT** . Boş olamaz. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml) { get; } | Dizindeki düğümde bulunan XML'i temsil eden bir dize alır.FlatOpc biçim. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping) { get; } | Bu yapılandırılmış belge etiketinin geçerli belgenin özel bir XML bölümünde XML data ile eşlenmesini temsil eden bir nesne alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear)() | Bu yapılandırılmış belge etiketinin içeriğini temizler ve tanımlanmışsa bir yer tutucu görüntüler. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly)() | Yalnızca bu SDT düğümünün kendisini kaldırır, ancak içeriğini belge ağacının içinde tutar. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Tümünü kaldırır[`SmartTag`](../smarttag) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol)(int, string) | Bir onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan sembolü ayarlar. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol)(int, string) | Bir onay kutusu içerik denetiminin işaretlenmemiş durumunu temsil etmek için kullanılan sembolü ayarlar. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Yapılandırılmış belge etiketleri (SDT'ler), müşteri tanımlı semantiğin yanı sıra davranışını ve görünümünü bir belgeye yerleştirmeye izin verir.

Bu sürümde Aspose.Words, davranış ve içeriği değiştirmek için bir dizi genel yöntem ve özellik sağlar.[`StructuredDocumentTag`](../structureddocumenttag) . SDT düğümlerinin bir belge içindeki özel XML paketleriyle eşlenmesi, [`XmlMapping`](./xmlmapping) Emlak.

[`StructuredDocumentTag`](../structureddocumenttag) bir belgede aşağıdaki yerlerde ortaya çıkabilir:

* Blok düzeyi - Paragraflar ve tablolar arasında, bir[`Body`](../../aspose.words/body) ,[`HeaderFooter`](../../aspose.words/headerfooter) , [`Comment`](../../aspose.words/comment) ,[`Footnote`](../../aspose.words.notes/footnote) veya bir[`Shape`](../../aspose.words.drawing/shape) düğüm.
* Row-level - Bir tablonun alt öğesi olarak bir tablodaki satırlar arasında[`Table`](../../aspose.words.tables/table) düğüm.
* Hücre düzeyi - Bir tablo satırındaki hücreler arasında, bir[`Row`](../../aspose.words.tables/row) düğüm.
* Satır içi düzey - İçerideki satır içi içerik arasında, bir çocuğun çocuğu olarak[`Paragraph`](../../aspose.words/paragraph).
* Bir başkasının içine yuvalanmış[`StructuredDocumentTag`](../structureddocumenttag).

### Örnekler

İçerik kontrol öğeleri için stiller ile nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, belgeden yapılandırılmış bir belge etiketine bir stil uygulamanın iki yolu verilmiştir.
// 1 - Belgenin stil koleksiyonundan bir stil nesnesi uygulayın:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Belgedeki bir stile ada göre başvuru yapın:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Ayrıca bakınız

* class [CompositeNode](../../aspose.words/compositenode)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
