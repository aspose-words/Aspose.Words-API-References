---
title: SubDocument Class
linktitle: SubDocument
articleTitle: SubDocument
second_title: .NET için Aspose.Words
description: Aspose.Words.SubDocument sınıfını keşfedin, sorunsuz entegrasyon ve gelişmiş belge işleme için harici belgeleri etkin bir şekilde yönetin ve referans alın.
type: docs
weight: 7020
url: /tr/net/aspose.words/subdocument/
---
## SubDocument class

Birini temsil eder**Alt Belge** - harici olarak depolanan bir belgeye referanstır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public class SubDocument : Node
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Geri Döndürür`doğru` eğer bu düğüm diğer düğümleri içerebiliyorsa. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words/subdocument/nodetype/) { get; } | Geri DöndürürSubDocument . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/subdocument/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Aspose.Words'ün bu sürümünde,`SubDocument`düğümler, bir alt belgeyi oluşturmak veya değiştirmek için genel methods ve özellikler sağlamaz. Bu sürümde instantiate yapamazsınız`SubDocument` Düğümleri silmek dışında var olanları değiştirmek veya düzenlemek.

`SubDocument` sadece bir çocuk olabilir[`Paragraph`](../paragraph/).

## Örnekler

Ana belgenin alt belgelerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Bu düğüm harici bir belgeye referans görevi görür ve içeriğine erişilemez.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Ayrıca bakınız

* class [Node](../node/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
