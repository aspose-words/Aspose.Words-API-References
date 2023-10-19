---
title: InlineStory Class
linktitle: InlineStory
articleTitle: InlineStory
second_title: Aspose.Words for .NET
description: Aspose.Words.InlineStory sınıf. Paragraflar ve tablolar içerebilen satır içi düzeydeki düğümler için temel sınıf C#'da.
type: docs
weight: 3270
url: /tr/net/aspose.words/inlinestory/
---
## InlineStory class

Paragraflar ve tablolar içerebilen satır içi düzeydeki düğümler için temel sınıf.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgedeki Düğümlerin Mantıksal Düzeyleri](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) dokümantasyon makalesi.

```csharp
public abstract class InlineStory : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Hikayedeki ilk paragrafı alır. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bu nesnenin bağlantı karakterinin yazı tipi formatlamasına erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | İadeler`doğru` bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | İadeler`doğru` çünkü bu düğüm alt düğümlere sahip olabilir. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | İadeler`doğru` değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse). |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Hikayedeki son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Hikayenin doğrudan alt öğeleri olan paragrafların bir koleksiyonunu alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype/) { get; } | Hikayenin türünü döndürür. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Hikayenin doğrudan alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Ziyaretçi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Son alt öğe bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atayı alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
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

`InlineStory` blok düzeyindeki düğümler için bir kapsayıcıdır[`Paragraph`](../paragraph/) Ve[`Table`](../../aspose.words.tables/table/).

Buradan türetilen sınıflar`InlineStory` kendi metinlerini (paragraflar ve tablolar) içerebilen satır içi düzey düğümlerdir. Örneğin, bir[`Comment`](../comment/) düğüm bir comment metnini ve bir[`Footnote`](../../aspose.words.notes/footnote/) dipnot metnini içerir.

## Örnekler

Bir paragrafa nasıl yorum ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // Microsoft Word'de, belge gövdesindeki bu yoruma sağ tıklayarak onu düzenleyebilir veya yanıtlayabiliriz.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Dipnotların nasıl ekleneceğini ve özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metin ekleyin ve ona bir dipnotla referans verin. Bu dipnotta küçük bir üst simge referansı yer alacaktır
// başvuruda bulunduğu metnin sonrasını işaretleyin ve sayfanın altındaki ana gövde metninin altında bir giriş oluşturun.
// Bu giriş dipnotun referans işaretini ve referans metnini içerecektir,
// bunu belge oluşturucunun "InsertFootnote" yöntemine aktaracağız.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Bu özellik "true" olarak ayarlanırsa dipnotumuzun referans işareti
// bölümün tüm dipnotları arasında dizini olacaktır.
// Bu ilk dipnot olduğundan referans işareti "1" olacaktır.
Assert.True(footnote.IsAuto);

 // Referans metnini düzenlemek için belge oluşturucuyu dipnotun içine taşıyabiliriz.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti ayarlayabiliriz.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// "IsAuto" bayrağı true olarak ayarlanmış bir yer imi yine de gerçek dizinini gösterecektir
// önceki yer imleri özel referans işaretlerini görüntülese bile, bu yer iminin referans işareti "3" olacaktır.
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Ayrıca bakınız

* class [CompositeNode](../compositenode/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
