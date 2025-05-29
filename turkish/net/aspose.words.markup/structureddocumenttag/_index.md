---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: .NET için Aspose.Words
description: Belgelerde etkili içerik kontrolü için Aspose.Words.Markup.StructuredDocumentTag sınıfını keşfedin. SDT özellikleriyle belge yönetiminizi geliştirin!
type: docs
weight: 4750
url: /tr/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Bir belgedeki yapılandırılmış bir belge etiketini (SDT veya içerik denetimi) temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | Yeni bir örneğini başlatır**Yapılandırılmış belge etiketi** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Yapılandırılmış bir belge etiketinin görünümünü alır/ayarlar. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Bu yapı bloğunun kategorisini belirtir**SDT** node. olamaz`hükümsüz` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Bu yapı bloğunun türünü belirtir**SDT** . olamaz`hükümsüz` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Bu takvimin türünü belirtir**SDT** . VarsayılanDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Onay Kutusunun geçerli durumunu alır/ayarlar**SDT** . Bu özelliğin varsayılan değeri:`YANLIŞ` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Girilen metne uygulanacak yazı tipi biçimlendirmesi**SDT** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Tarihlerin görüntülendiği biçimi temsil eden dize. |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Bu ekranda görüntülenen tarih için dil biçimini ayarlamayı/almayı sağlar.**SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Bir tarih SDT'sinin saklandığı tarihin biçimini alır/ayarlar**SDT** Belgenin veri deposundaki bir XML düğümüne bağlıdır. Varsayılan değerDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Girilen metnin son karakterine uygulanacak yazı tipi biçimlendirmesi**SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Bu dosyaya en son girilen tam tarih ve saati belirtir**SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Bunun için benzersiz, salt okunur, kalıcı bir sayısal Kimlik belirtir**SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Bu içeriğin ne olduğunu belirtir**SDT** yer tutucu text (SDT içindeki normal metin içeriklerinin aksine) içerecek şekilde yorumlanacaktır. |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Bunun olup olmadığını belirtir**SDT** içerikleri değiştirildiğinde WordProcessingML belgesinden kaldırılacaktır. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Bu seviyeyi alır**SDT** belge ağacında meydana gelir. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Alır[`SdtListItemCollection`](../sdtlistitemcollection/) bununla ilişkili**SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | olarak ayarlandığında`doğru` , bu özellik bir kullanıcının bunu silmesini engelleyecektir**SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | olarak ayarlandığında`doğru` , bu özellik bir kullanıcının bu içeriği düzenlemesini engelleyecektir**SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Bunun olup olmadığını belirtir**SDT** birden fazla satır metne izin verir. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | Geri DöndürürStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Şunu alır:[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) Bu SDT çalıştırma içeriği boş olduğunda görüntülenmesi gereken yer tutucu metni içeren, ilişkili eşlenen XML öğesi, belirtilen şekilde boştur[`XmlMapping`](./xmlmapping/) element veya[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) eleman`doğru` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Adını alır veya ayarlar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) yer tutucu metin içeren. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Bunun türünü alır**Yapılandırılmış belge etiketi** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Yapılandırılmış belge etiketinin Stilini alır veya ayarlar. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Yapılandırılmış belge etiketine uygulanan stilin adını alır veya ayarlar. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Geçerli SDT düğümüyle ilişkili bir etiketi belirtir. Şu şekilde olamaz:`hükümsüz` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Bu ile ilişkili dostça adı belirtir**SDT** . olamaz`hükümsüz` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Düğümün içinde bulunan XML'i temsil eden bir dize alırFlatOpc biçim. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | Düğümün içinde bulunan XML'i temsil eden bir dize alırFlatOpc format. Bunun aksine[`WordOpenXML`](./wordopenxml/) özellik, bu yöntem içerikle ilgili olmayan parçaları hariç tutan soyulmuş bir belge oluşturur. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Bu yapılandırılmış belge etiketinin geçerli belgenin özel bir XML bölümündeki XML data eşlemesini temsil eden bir nesne alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | StructuredDocumentTag'ın sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | StructuredDocumentTag'in başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Bu yapılandırılmış belge etiketinin içeriğini temizler ve tanımlanmışsa bir yer tutucu görüntüler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Belirtilen alt düğümü kaldırır. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Yalnızca bu SDT düğümünü kaldırır, ancak içeriğini belge ağacının içinde tutar. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | Bir onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan simgeyi ayarlar. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | Bir onay kutusu içerik denetiminin işaretlenmemiş durumunu temsil etmek için kullanılan simgeyi ayarlar. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Yapılandırılmış belge etiketleri (SDT'ler), müşteri tarafından tanımlanan semantiğin yanı sıra its davranışını ve görünümünü bir belgeye yerleştirmeye olanak tanır.

Bu sürümde Aspose.Words, davranış ve içeriği manipüle etmek için bir dizi genel yöntem ve özellik sağlar.`StructuredDocumentTag` . SDT düğümlerinin bir belge içindeki özel XML paketlerine eşlenmesi, kullanılarak gerçekleştirilebilir[`XmlMapping`](./xmlmapping/) mülk.

`StructuredDocumentTag` Bir belgede aşağıdaki yerlerde bulunabilir:

* Blok düzeyi - Paragraflar ve tablolar arasında, bir alt öğe olarak[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) veya bir[`Shape`](../../aspose.words.drawing/shape/) düğüm.
* Satır düzeyi - Bir tablodaki satırlar arasında, bir alt satır olarak[`Table`](../../aspose.words.tables/table/) düğüm.
* Hücre düzeyi - Bir tablo satırındaki hücreler arasında, bir hücrenin çocuğu olarak[`Row`](../../aspose.words.tables/row/) düğüm.
* Satır içi düzey - Bir alt öğenin bir parçası olarak, satır içi içerik arasında[`Paragraph`](../../aspose.words/paragraph/).
* Birbirinin içine yerleştirilmiş`StructuredDocumentTag`.

## Örnekler

İçerik kontrol öğeleri için stillerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, bir belgeden yapılandırılmış belge etiketine bir stil uygulamanın iki yolu bulunmaktadır.
// 1 - Belgenin stil koleksiyonundan bir stil nesnesi uygula:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Belgedeki bir stile adıyla başvuruda bulunun:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Ayrıca bakınız

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
