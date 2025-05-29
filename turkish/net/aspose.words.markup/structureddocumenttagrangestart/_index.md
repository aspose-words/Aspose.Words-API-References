---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: .NET için Aspose.Words
description: Yapılandırılmış belgelerde sorunsuz çok bölümlü içerik yönetimini sağlayan Aspose.Words.Markup.StructuredDocumentTagRangeStart sınıfını keşfedin.
type: docs
weight: 4780
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Bir başlangıcı temsil eder**menzilli** çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. Ayrıca bkz.[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | Yeni bir örneğini başlatır**Yapılandırılmış belge etiketi aralığı başlangıcı** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttagrangestart/appearance/) { get; set; } | Yapılandırılmış belge etiketinin görünümünü alır veya ayarlar. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Bu yapılandırılmış belge etiketi için benzersiz, salt okunur, kalıcı bir sayısal Kimlik belirtir. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Geri Döndürür`doğru` eğer bu düğüm diğer düğümleri içerebiliyorsa. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Bu yapılandırılmış belge etiketinin içeriğinin, yer tutucu metni (yapılandırılmış belge etiketindeki normal metin içeriklerinin aksine) içerecek şekilde yorumlanıp yorumlanmayacağını belirtir. |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | stdContent aralığındaki son çocuğu alır. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Bu yapılandırılmış belge etiketi aralığının belge ağacında hangi düzeyde başladığını alır. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | olarak ayarlandığında`doğru` , bu özellik bir kullanıcının bu yapılandırılmış belge etiketini silmesini engelleyecektir. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | olarak ayarlandığında`doğru` , bu özellik bir kullanıcının bu yapılandırılmış belge etiketinin içeriğini düzenlemesini yasaklayacaktır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | Geri DöndürürStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Şunu alır:[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)yer tutucu metni içeren ve bu yapılandırılmış belge etiketinin içeriği boş olduğunda görüntülenmesi gereken bu metin, ilişkili eşlenen XML öğesi belirtilen şekilde boştur aracılığıyla[`XmlMapping`](./xmlmapping/) eleman veya[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) eleman`doğru` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Adını alır veya ayarlar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) yer tutucu metin içeren. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Aralık sonunu belirtir.[`StructuredDocumentTag`](../structureddocumenttag/) aralıklı yapılandırılmış bir belge etiketidir. Aksi takdirde döner`hükümsüz` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Bu yapılandırılmış belge etiketinin türünü alır. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Geçerli yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. Olamaz`hükümsüz` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Bu yapılandırılmış belge etiketiyle ilişkili kolay adı belirtir. olamaz`hükümsüz` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Düğümün içinde bulunan XML'i temsil eden bir dize alırFlatOpc biçim. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/) { get; } | Düğümün içinde bulunan XML'i temsil eden bir dize alırFlatOpc format. Bunun aksine[`WordOpenXML`](./wordopenxml/) özellik, bu yöntem içerikle ilgili olmayan parçaları hariç tutan soyulmuş bir belge oluşturur. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Bu yapılandırılmış belge etiketi aralığının, geçerli belgenin özel bir XML bölümündeki XML data eşlemesini temsil eden bir nesne alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | Belirtilen düğümü stdContent aralığının sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Bu aralık başlangıç düğümü ile aralık bitiş düğümü arasındaki tüm düğümleri kaldırır. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Yapılandırılmış belge etiketinin bu aralık başlangıcını ve uygun aralık bitiş düğümlerini kaldırır, ancak içeriğini belge ağacının içinde tutar. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Şunun hemen çocuğu olabilir:[`Body`](../../aspose.words/body/) düğüm**sadece** .

## Örnekler

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Ayrıca bakınız

* class [Node](../../aspose.words/node/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
