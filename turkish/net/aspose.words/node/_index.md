---
title: Node Class
linktitle: Node
articleTitle: Node
second_title: .NET için Aspose.Words
description: Tüm Word belge düğümlerinin temelini oluşturan Aspose.Words.Node sınıfını keşfedin; bu sınıf, kusursuz belge düzenleme ve özelleştirme olanağı sağlar.
type: docs
weight: 4860
url: /tr/net/aspose.words/node/
---
## Node class

Bir Word belgesinin tüm düğümleri için temel sınıf.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public abstract class Node
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Geri Döndürür`doğru` eğer bu düğüm diğer düğümleri içerebiliyorsa. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor_1)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*Node*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*Node*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/#tostring_1)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/#tostring_2)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(*[NodeType](../nodetype/)*) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren bir yardımcı yöntem. |

## Notlar

Bir belge, DOM veya XmlDocument'a benzer şekilde düğümlerden oluşan bir ağaç olarak temsil edilir.

Daha fazla bilgi için Composite tasarım desenine bakın.

The`Node` sınıf:

* Çocuk düğüm arayüzünü tanımlar.
* Düğümleri ziyaret etmek için arayüzü tanımlar.
* Varsayılan klonlama yeteneği sağlar.
* Üst düğüm ve sahip belge mekanizmalarını uygular.
* Kardeş düğümlere erişimi uygular.

## Örnekler

Belirli bir türdeki tüm alt düğümlerin bileşik bir düğümden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Bu düğümü sildikten sonra ona geçmek istersek, bir sonraki kardeş düğümü bir değişken olarak kaydet.
    Node nextNode = curNode.NextSibling;

    // Bir bölüm gövdesi Paragraf ve Tablo düğümlerini içerebilir.
    // Eğer düğüm bir Tablo ise, onu ana düğümden kaldır.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

Bileşik bir düğümün nasıl klonlanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Aşağıda bir bileşik düğümü klonlamanın iki yolu bulunmaktadır.
// 1 - Bir düğümün klonunu oluştur ve ayrıca onun her bir alt düğümünün bir klonunu oluştur.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Herhangi bir çocuğu olmadan sadece kendi başına bir düğümün klonunu oluştur.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

Bir bileşik düğümün alt düğüm koleksiyonunda nasıl dolaşılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına iki çalışma ve bir şekil alt düğüm olarak ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId' öğesinin bir çıktı dosyasına kaydedilmediğini ve yalnızca düğümün yaşam süresi boyunca var olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın hemen altındaki alt öğelerin koleksiyonunda yineleme yapın,
// ve içinde bulduğumuz herhangi bir koşuyu veya şekli yazdırırız.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
