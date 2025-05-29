---
title: OfficeMath Class
linktitle: OfficeMath
articleTitle: OfficeMath
second_title: .NET için Aspose.Words
description: Denklemler ve matrisler gibi Office Math nesnelerini kolaylıkla oluşturmak ve yönetmek için tasarlanmış Aspose.Words.Math.OfficeMath sınıfını keşfedin.
type: docs
weight: 4810
url: /tr/net/aspose.words.math/officemath/
---
## OfficeMath class

Fonksiyon, denklem, matris veya benzeri bir Office Math nesnesini temsil eder. Matematiksel metin, yer imleri, yorumlar ve diğer alt öğeleri içerebilir.`OfficeMath`örnekler ve bazı diğer düğümler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[OfficeMath ile Çalışma](https://docs.aspose.com/words/net/working-with-officemath/) belgeleme makalesi.

```csharp
public class OfficeMath : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | Bir denklemin metinle aynı satırda mı yoksa kendi satırında mı görüntüleneceğini temsil eden Office Math görüntüleme biçimi türünü alır/ayarlar. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | Office Math gerekçesini alır/ayarlar. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | Türü alır[`MathObjectType`](./mathobjecttype/)bu Office Math nesnesinin. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | Geri DöndürürOfficeMath . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words.math/officemath/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Ofis matematiğinin sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words.math/officemath/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Ofis matematiğinin başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | Bu denklemi bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Aspose.Words'ün bu sürümünde,`OfficeMath` düğümler, bir düğüm oluşturmak veya değiştirmek için genel methods ve özellikler sağlamaz`OfficeMath` nesne. Bu sürümde instantiate yapamazsınızMath Düğümleri silmek dışında var olanları değiştirmek veya düzenlemek.

`OfficeMath` sadece bir çocuk olabilir[`Paragraph`](../../aspose.words/paragraph/).

## Örnekler

Ofis matematik görüntüleme biçimlendirmesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Diğer OfficeMath düğümlerinin çocuğu olan OfficeMath düğümleri her zaman satır içidir.
// Üzerinde çalıştığımız düğüm, konumunu ve görüntüleme türünü değiştirecek temel düğümdür.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// OfficeMath düğümünün konumunu ve görüntüleme türünü değiştirin.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Ayrıca bakınız

* class [CompositeNode](../../aspose.words/compositenode/)
* ad alanı [Aspose.Words.Math](../../aspose.words.math/)
* toplantı [Aspose.Words](../../)
