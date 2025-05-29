---
title: DocumentBase Class
linktitle: DocumentBase
articleTitle: DocumentBase
second_title: .NET için Aspose.Words
description: Word belgelerini ve sözlüklerini kolaylıkla ve verimli bir şekilde oluşturmak ve yönetmek için temel olan Aspose.Words.DocumentBase sınıfını keşfedin.
type: docs
weight: 650
url: /tr/net/aspose.words/documentbase/
---
## DocumentBase class

Bir Word belgesinin ana belgesi ve sözlük belgesi için soyut temel sınıfı sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Belgenin arka plan şeklini alır veya ayarlar.`hükümsüz` . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Bu örneği alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Belgede tanımlanan dipnot/sonnot ayırıcılarına erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Belgede kullanılan liste biçimlendirmesine erişim sağlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, daha basit bir sürümüdür[`BackgroundShape`](./backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Harici kaynakların nasıl yükleneceğini kontrol etmenizi sağlar. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Belgede tanımlanan stil koleksiyonunu döndürür. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Çeşitli belge işleme prosedürleri sırasında, veri veya biçimlendirme sadakat kaybına neden olabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXEnd yöntemini çağırır. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXStart yöntemini çağırır. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(*[Node](../node/), bool*) | Başka bir belgeden bir düğümü geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Biçimlendirmeyi kontrol etme seçeneğiyle başka bir belgeden geçerli belgeye bir düğüm aktarır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../node/) XPath ifadesiyle eşleşen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Aspose.Words, bir Word belgesini düğümlerden oluşan bir ağaç olarak temsil eder.`DocumentBase` a belgenin diğer tüm düğümlerini içeren ağacın kök düğümüdür.

`DocumentBase` ayrıca belge genelindeki bilgileri de depolar, örneğin[`Styles`](./styles/) ve [`Lists`](./lists/) ağaç düğümlerinin atıfta bulunabileceği.

## Örnekler

DocumentBase alt sınıflarının nasıl başlatılacağını gösterir.

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
