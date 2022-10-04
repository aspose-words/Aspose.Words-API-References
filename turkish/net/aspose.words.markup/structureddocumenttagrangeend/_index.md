---
title: StructuredDocumentTagRangeEnd
second_title: Aspose.Words for .NET API Referansı
description: Bir sonunu temsil eder menzilli çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. Ayrıca bkz.StructuredDocumentTagRangeStart./structureddocumenttagrangestart/ düğüm.
type: docs
weight: 3840
url: /tr/net/aspose.words.markup/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd class

Bir sonunu temsil eder **menzilli** çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. Ayrıca bkz.[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) düğüm.

```csharp
public class StructuredDocumentTagRangeEnd : Node
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [StructuredDocumentTagRangeEnd](structureddocumenttagrangeend/)(DocumentBase, int) | Yeni bir örneğini başlatır **Yapılandırılmış belge etiketi aralığı sonu** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Id](../../aspose.words.markup/structureddocumenttagrangeend/id/) { get; } | Bunun için benzersiz bir salt okunur kalıcı sayısal kimlik belirtir **YapılandırılmışBelgeEtiketAralığı** node. Karşılık gelen[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) düğüm aynı[`Id`](../structureddocumenttagrangestart/id/) . |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangeend/nodetype/) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangeend/accept/)(DocumentVisitor) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
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
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
