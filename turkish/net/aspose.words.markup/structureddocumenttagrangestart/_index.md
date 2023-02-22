---
title: Class StructuredDocumentTagRangeStart
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.StructuredDocumentTagRangeStart sınıf. Bir başlangıcı temsil eder menzilli çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. Ayrıca bkz.StructuredDocumentTagRangeEnd .
type: docs
weight: 3850
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Bir başlangıcı temsil eder **menzilli** çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. Ayrıca bkz.[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(DocumentBase, SdtType) | Yeni bir örneğini başlatır **Yapılandırılmış belge etiketi aralığı başlangıcı** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes/) { get; } | Bu aralık başlangıç düğümü ile aralık bitiş düğümü arasındaki tüm düğümleri alır. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Bu yapılandırılmış belge etiketi için benzersiz bir salt okunur kalıcı sayısal kimlik belirtir. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Bu yapılandırılmış belge etiketinin içeriğinin, (yapılandırılmış belge etiketi içindeki normal metin içeriklerinin aksine) yer tutucu metin içerecek şekilde yorumlanıp yorumlanmayacağını belirtir. |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | stdContent aralığındaki son çocuğu alır. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Bu yapılandırılmış belge etiketi aralığı başlangıcının belge ağacında gerçekleştiği düzeyi alır. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketini silmesini engeller. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketinin içeriğini düzenlemesini engeller. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) bu yapılandırılmış belge etiketi çalıştırma içeriği boş olduğunda görüntülenmesi gereken yer tutucu metni içeren, ilişkili eşlenen XML öğesi, belirtilen aracılığıyla boş olduğunda[`XmlMapping`](./xmlmapping/) eleman veya[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) eleman doğrudur. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Adını alır veya ayarlar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) yer tutucu metni içeren. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | StructuredDocumentTag bir aralıklı yapılandırılmış belge etiketiyse, aralığın sonunu belirtir. Aksi takdirde null. döndürür |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Bu yapılandırılmış belge etiketinin türünü alır. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Geçerli yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. Boş olamaz. |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Bu yapılandırılmış belge etiketiyle ilişkili kolay adı belirtir. Boş olamaz. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Dizindeki düğümde bulunan XML'i temsil eden bir dize alır.FlatOpc biçim. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Geçerli belgenin özel bir XML bölümünde bu yapılandırılmış belge etiketi aralığının XML data ile eşlenmesini temsil eden bir nesne alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(DocumentVisitor) |  |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(Node) | Belirtilen düğümü stdContent aralığının sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(NodeType, bool) | Belirtilen türlerle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Bu aralık başlangıç düğümü ile aralık bitiş düğümü arasındaki tüm düğümleri kaldırır. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Yapılandırılmış belge etiketinin bu aralık başlangıcını ve uygun aralık bitiş düğümlerini kaldırır, ancak içeriğini belge ağacının içinde tutar. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Hemen alt öğesi olabilir[`Body`](../../aspose.words/body/) düğüm **sadece** .

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


