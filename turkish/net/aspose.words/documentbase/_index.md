---
title: DocumentBase
second_title: Aspose.Words for .NET API Referansı
description: Bir ana belge için soyut temel sınıf ve bir Word belgesinin sözlük belgesi sağlar.
type: docs
weight: 430
url: /tr/net/aspose.words/documentbase/
---
## DocumentBase class

Bir ana belge için soyut temel sınıf ve bir Word belgesinin sözlük belgesi sağlar.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Belgenin arka plan şeklini alır veya ayarlar. null. olabilir |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| override [Document](../../aspose.words/documentbase/document/) { get; } |  |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk alt öğesini alır. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son alt öğesini alır. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Belgede kullanılan liste formatına erişim sağlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, aşağıdakilerin daha basit bir sürümüdür:[`BackgroundShape`](./backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Harici kaynakların nasıl yüklendiğini kontrol etmeye izin verir. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Belgede tanımlanan stillerin bir koleksiyonunu döndürür. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Verilerde veya biçimlendirme aslına uygunluk kaybına neden olabilecek bir sorun algılandığında çeşitli belge işleme prosedürleri sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(Node, bool) | Bir düğümü başka bir belgeden geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(Node, bool, ImportFormatMode) | Biçimlendirmeyi kontrol etme seçeneği ile bir düğümü başka bir belgeden geçerli belgeye aktarır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Aspose.Words bir Word belgesini bir düğüm ağacı olarak temsil eder.[`DocumentBase`](./documentbase/) belgenin diğer tüm düğümlerini içeren ağacın bir kök düğümüdür.

[`DocumentBase`](./documentbase/) gibi belge çapındaki bilgileri de depolar.[`Styles`](./styles/) ve [`Lists`](./lists/) ağaç düğümlerinin başvurabileceği.

### Örnekler

DocumentBase'in alt sınıflarının nasıl başlatılacağını gösterir.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### Ayrıca bakınız

* class [CompositeNode](../compositenode/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
