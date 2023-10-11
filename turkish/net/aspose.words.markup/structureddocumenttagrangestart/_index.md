---
title: Class StructuredDocumentTagRangeStart
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.StructuredDocumentTagRangeStart sınıf. Bir başlangıcı temsil eder aralıklı çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. Ayrıca bkz.StructuredDocumentTagRangeEnd .
type: docs
weight: 4090
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Bir başlangıcı temsil eder **aralıklı** çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. Ayrıca bkz.[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokümantasyon makalesi.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(DocumentBase, SdtType) | Yeni bir örneğini başlatır **Yapılandırılmış belge etiketi aralığı başlangıcı** class. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes/) { get; } | Bu aralık başlangıç düğümü ile aralık bitiş düğümü arasındaki tüm düğümleri alır. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Bu yapılandırılmış belge etiketi için benzersiz, salt okunur, kalıcı bir sayısal kimlik belirtir. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | İadeler`doğru` bu düğüm başka düğümler içeriyorsa. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Bu yapılandırılmış belge etiketinin içeriğinin, (yapılandırılmış belge etiketi içindeki normal metin içeriklerinin aksine) yer tutucu metni içerecek şekilde yorumlanıp yorumlanmayacağını belirtir. |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | StdContent aralığındaki son alt öğeyi alır. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Bu yapılandırılmış belge etiketi aralığının belge ağacında başlayacağı düzeyi alır. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | Olarak ayarlandığında`doğru` , bu özellik kullanıcının bu yapılandırılmış belge etiketini silmesini yasaklar. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | Olarak ayarlandığında`doğru` , bu özellik kullanıcının bu yapılandırılmış belge etiketinin içeriğini düzenlemesini yasaklar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | İadelerStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Alır[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)bu yapılandırılmış belge etiketi çalıştırma içerikleri boş olduğunda görüntülenmesi gereken yer tutucu metni içerir, ilgili eşlenen XML öğesi, belirtilen aracılığıyla boştur[`XmlMapping`](./xmlmapping/) eleman veya[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) eleman`doğru` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Adını alır veya ayarlar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) yer tutucu metni içerir. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../../aspose.words/range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Aşağıdaki durumlarda aralığın sonunu belirtir:[`StructuredDocumentTag`](../structureddocumenttag/) aralıklı yapılandırılmış bir belge etiketidir. Aksi halde şunu döndürür`hükümsüz` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Bu yapılandırılmış belge etiketinin türünü alır. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Geçerli yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. Yapılamaz`hükümsüz` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Bu yapılandırılmış belge etiketiyle ilişkili kolay adı belirtir. Yapılamaz`hükümsüz` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Düğümdeki düğümün içerdiği XML'i temsil eden bir dize alır.FlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Bu yapılandırılmış belge etiketi aralığının, geçerli belgenin özel bir XML bölümündeki XML data ile eşlenmesini temsil eden bir nesne alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(DocumentVisitor) | Ziyaretçi kabul eder. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(Node) | Belirtilen düğümü stdContent aralığının sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atayı alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(NodeType, bool) | Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Bu aralık başlangıç düğümü ile aralık bitiş düğümü arasındaki tüm düğümleri kaldırır. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Yapılandırılmış belge etiketinin, bu aralık başlangıç ve uygun aralık sonu düğümlerini kaldırır, ancak içeriğini belge ağacının içinde tutar. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Birincil alt öğe olabilir[`Body`](../../aspose.words/body/) düğüm **sadece** .

### Örnekler

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


