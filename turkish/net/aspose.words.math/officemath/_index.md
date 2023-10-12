---
title: Class OfficeMath
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Math.OfficeMath sınıf. Fonksiyon denklem matris veya benzeri bir Office Math nesnesini temsil eder. Matematiksel metinler yer imleri yorumlar ve diğer öğeler de dahil olmak üzere alt öğeler içerebilirOfficeMathörnekler ve diğer bazı düğümler.
type: docs
weight: 4120
url: /tr/net/aspose.words.math/officemath/
---
## OfficeMath class

Fonksiyon, denklem, matris veya benzeri bir Office Math nesnesini temsil eder. Matematiksel metinler, yer imleri, yorumlar ve diğer öğeler de dahil olmak üzere alt öğeler içerebilir`OfficeMath`örnekler ve diğer bazı düğümler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[OfficeMath'le çalışmak](https://docs.aspose.com/words/net/working-with-officemath/) dokümantasyon makalesi.

```csharp
public class OfficeMath : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | Bir denklemin text ile satır içi olarak mı yoksa kendi satırında mı görüntüleneceğini temsil eden Office Math görüntüleme biçimi türünü alır/ayarlar. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | İadeler`doğru` bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | İadeler`doğru` çünkü bu düğüm alt düğümlere sahip olabilir. |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | Office Matematik gerekçesini alır/ayarlar. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | Türü alır[`MathObjectType`](./mathobjecttype/) bu Office Math nesnesinin. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | İadelerOfficeMath . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../../aspose.words/range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(DocumentVisitor) | Ziyaretçi kabul eder. |
| override [AcceptEnd](../../aspose.words.math/officemath/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.math/officemath/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atayı alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | Bu denklemi bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/)Geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Aspose.Words'ün bu sürümünde,`OfficeMath` düğümler, bir ağ oluşturmak veya değiştirmek için genel yöntemler ve özellikler sağlamaz`OfficeMath` nesne. Bu sürümde, örnekleme işlemini gerçekleştiremezsiniz.Math düğümleri silin veya bunları silmek dışında mevcut olanı değiştirin.

`OfficeMath` sadece çocuğu olabilir[`Paragraph`](../../aspose.words/paragraph/).

### Örnekler

Ofis matematik ekranı formatının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Diğer OfficeMath düğümlerinin çocukları olan OfficeMath düğümleri her zaman satır içidir.
// Çalıştığımız düğüm, konumunu ve görüntüleme türünü değiştirecek temel düğümdür.
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


