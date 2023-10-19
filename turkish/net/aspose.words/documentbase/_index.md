---
title: DocumentBase Class
linktitle: DocumentBase
articleTitle: DocumentBase
second_title: Aspose.Words for .NET
description: Aspose.Words.DocumentBase sınıf. Bir ana belge ve bir Word belgesinin sözlük belgesi için soyut temel sınıfı sağlar C#'da.
type: docs
weight: 440
url: /tr/net/aspose.words/documentbase/
---
## DocumentBase class

Bir ana belge ve bir Word belgesinin sözlük belgesi için soyut temel sınıfı sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokümantasyon makalesi.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Belgenin arka plan şeklini alır veya ayarlar. Olabilir`hükümsüz` . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Bu örneği alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | İadeler`doğru` bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | İadeler`doğru` çünkü bu düğüm alt düğümlere sahip olabilir. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Belgede kullanılan liste formatına erişim sağlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, daha basit bir versiyonudur[`BackgroundShape`](./backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Harici kaynakların nasıl yüklendiğini kontrol etmeye izin verir. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Belgede tanımlanan stillerin bir koleksiyonunu döndürür. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Çeşitli belge işleme prosedürleri sırasında, verilerde veya formatta uygunluk kaybıyla sonuçlanabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Ziyaretçi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atayı alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(*[Node](../node/), bool*) | Başka bir belgedeki bir düğümü geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Biçimlendirmeyi kontrol etme seçeneğiyle birlikte başka bir belgedeki bir düğümü geçerli belgeye aktarır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Alt düğüm dizisinde belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Belirtilen düğümü, belirtilen referans düğümünün hemen sonrasına ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Belirtilen düğümü, belirtilen referans düğümünün hemen öncesine ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/)Geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../node/) XPath ifadesiyle eşleşen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Aspose.Words, bir Word belgesini bir düğüm ağacı olarak temsil eder.`DocumentBase` belgenin tüm diğer düğümlerini içeren ağacın a kök düğümüdür.

`DocumentBase` ayrıca belge genelindeki bilgileri de saklar:[`Styles`](./styles/) ve [`Lists`](./lists/) ağaç düğümlerinin başvurabileceği.

## Örnekler

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
