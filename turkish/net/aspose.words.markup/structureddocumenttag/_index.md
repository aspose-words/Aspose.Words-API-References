---
title: Class StructuredDocumentTag
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.StructuredDocumentTag sınıf. Bir belgedeki yapılandırılmış belge etiketini SDT veya içerik kontrolü temsil eder.
type: docs
weight: 4060
url: /tr/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Bir belgedeki yapılandırılmış belge etiketini (SDT veya içerik kontrolü) temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokümantasyon makalesi.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(DocumentBase, SdtType, MarkupLevel) | Yeni bir örneğini başlatır **Yapılandırılmış belge etiketi** class. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Yapılandırılmış bir belge etiketinin görünümünü alır/ayarlar. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Bunun için yapı taşının kategorisini belirtir **SDT** node. Olamaz`hükümsüz` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Bunun için yapı taşının türünü belirtir **SDT** . Olamaz`hükümsüz` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Bunun için takvim türünü belirtir **SDT** . Varsayılan:Default |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Onay Kutusunun geçerli durumunu alır/ayarlar **SDT** . Bu özelliğin varsayılan değeri:`YANLIŞ` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Girilen metne uygulanacak yazı tipi formatı **SDT** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Tarihlerin görüntülendiği biçimi temsil eden dize. Yapılamaz`hükümsüz` . İngilizce (ABD) için tarihler "aa/gg/yyyy"dir |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Burada görüntülenen tarih için dil biçimini ayarlamanıza/almanıza olanak tanır. **SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | SDT'nin saklandığı tarih için tarihin biçimini alır/ayarlar. **SDT**belgenin veri deposundaki bir XML düğümüne bağlanır. Varsayılan değer:DateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Girilen metnin son karakterine uygulanacak yazı tipi formatı **SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Buna en son girilen tam tarih ve saati belirtir **SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | İadeler`doğru` bu düğümün herhangi bir alt düğümü varsa. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Bunun için benzersiz bir salt okunur kalıcı sayısal kimlik belirtir **SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | İadeler`doğru` çünkü bu düğüm alt düğümlere sahip olabilir. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Bunun içeriğinin olup olmadığını belirtir. **SDT**yer tutucu text 'yi (SDT içindeki normal metin içeriklerinin aksine) içerecek şekilde yorumlanacaktır. |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Bunun olup olmadığını belirtir **SDT** içeriği değiştirildiğinde WordProcessingML belgesinden kaldırılacaktır. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Bunun hangi düzeyde olduğunu alır **SDT** belge ağacında oluşur. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Alır[`SdtListItemCollection`](../sdtlistitemcollection/) bununla ilişkili **SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | Olarak ayarlandığında`doğru` , bu özellik kullanıcının bunu silmesini yasaklayacak **SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | Olarak ayarlandığında`doğru` , bu özellik kullanıcının bu içeriği düzenlemesini yasaklar **SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Bunun olup olmadığını belirtir **SDT** birden fazla metin satırına izin verir. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | İadelerStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Alır[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)Bu SDT çalıştırma içerikleri boş olduğunda görüntülenmesi gereken yer tutucu metni içeren, ilişkili eşlenen XML öğesi,[`XmlMapping`](./xmlmapping/) element veya[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) eleman`doğru` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Adını alır veya ayarlar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) yer tutucu metni içerir. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../../aspose.words/range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Bunun türünü alır **Yapılandırılmış belge etiketi** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Yapılandırılmış belge etiketinin Stilini alır veya ayarlar. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Yapılandırılmış belge etiketine uygulanan stilin adını alır veya ayarlar. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Geçerli SDT düğümüyle ilişkili bir etiketi belirtir. Yapılamaz`hükümsüz` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Bununla ilişkili kolay adı belirtir **SDT** . Olamaz`hükümsüz` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Düğümdeki düğümün içerdiği XML'i temsil eden bir dize alır.FlatOpc format. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | Düğümdeki düğümün içerdiği XML'i temsil eden bir dize alır.FlatOpc format. Şunun aksine[`WordOpenXML`](./wordopenxml/)özelliğinden yararlanarak, bu yöntem, içerikle ilgili olmayan bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Bu yapılandırılmış belge etiketinin, geçerli belgenin özel bir XML bölümündeki XML data ile eşlenmesini temsil eden bir nesne alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(DocumentVisitor) | Ziyaretçi kabul eder. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Bu yapılandırılmış belge etiketinin içeriğini temizler ve tanımlanmışsa bir yer tutucu görüntüler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atayı alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisinde belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Yalnızca bu SDT düğümünün kendisini kaldırır ancak içeriğini belge ağacının içinde tutar. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../smarttag/)Geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(int, string) | Onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan sembolü ayarlar. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(int, string) | Onay kutusu içerik denetiminin işaretlenmemiş durumunu temsil etmek için kullanılan sembolü ayarlar. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Yapılandırılmış belge etiketleri (SDT'ler), müşteri tanımlı semantiğin yanı sıra its davranışını ve görünümünü bir belgeye yerleştirmeye olanak tanır.

Bu sürümde Aspose.Words, davranışını ve içeriğini değiştirmek için bir dizi genel yöntem ve özellik sağlar.`StructuredDocumentTag` . SDT düğümlerinin bir belge içindeki özel XML paketleriyle eşlenmesi, kullanılarak gerçekleştirilebilir.[`XmlMapping`](./xmlmapping/) mülk.

`StructuredDocumentTag` bir belgede aşağıdaki yerlerde bulunabilir:

* Blok düzeyinde - Paragraflar ve tablolar arasında, bir çocuğun çocuğu olarak[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) veya bir[`Shape`](../../aspose.words.drawing/shape/) düğüm.
* Satır düzeyi - Bir tablodaki satırlar arasında, bir öğenin alt öğesi olarak[`Table`](../../aspose.words.tables/table/) düğüm.
* Hücre düzeyi - Bir tablo satırındaki hücreler arasında, bir alt öğe olarak[`Row`](../../aspose.words.tables/row/) düğüm.
* Satır içi düzey - Bir çocuğun çocuğu olarak içerideki satır içi içerik arasında[`Paragraph`](../../aspose.words/paragraph/).
* Başka birinin içine yerleştirilmiş`StructuredDocumentTag`.

### Örnekler

İçerik kontrol öğelerine ilişkin stillerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda belgeden yapılandırılmış belge etiketine stil uygulamanın iki yolu verilmiştir.
// 1 - Belgenin stil koleksiyonundan bir stil nesnesi uygulayın:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Belgedeki bir stile ada göre referans verin:
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


