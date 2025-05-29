---
title: InlineStory Class
linktitle: InlineStory
articleTitle: InlineStory
second_title: .NET için Aspose.Words
description: Belgelerinizdeki paragrafların ve tabloların sorunsuz bir şekilde entegre edilmesini sağlayan, satır içi düğümler için temel bir temel olan Aspose.Words.InlineStory sınıfını keşfedin.
type: docs
weight: 3720
url: /tr/net/aspose.words/inlinestory/
---
## InlineStory class

Paragraflar ve tablolar içerebilen satır içi düzey düğümler için temel sınıf.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgedeki Düğümlerin Mantıksal Düzeyleri](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) belgeleme makalesi.

```csharp
public abstract class InlineStory : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Hikayedeki ilk paragrafı alır. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bu nesnenin bağlantı karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse). |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse). |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Hikayedeki son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Hikayenin doğrudan alt öğeleri olan paragrafların bir koleksiyonunu alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype/) { get; } | Hikayenin türünü döndürür. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Hikayenin doğrudan alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXEnd yöntemini çağırır. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXStart yöntemini çağırır. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
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

`InlineStory` blok düzeyindeki düğümler için bir kapsayıcıdır[`Paragraph`](../paragraph/) Ve[`Table`](../../aspose.words.tables/table/).

Türetilen sınıflar`InlineStory` kendi metinlerini (paragraflar ve tablolar) içerebilen satır içi düzeydeki düğümlerdir. Örneğin, bir[`Comment`](../comment/) düğüm bir comment metnini ve bir[`Footnote`](../../aspose.words.notes/footnote/) Dipnot metnini içerir.

## Örnekler

Bir paragrafa yorum eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // Microsoft Word'de, bu yorumu belge gövdesinde sağ tıklayarak düzenleyebilir veya yanıtlayabiliriz.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Dipnotların nasıl ekleneceğini ve özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metin ekleyin ve bir dipnotla referans verin. Bu dipnot, küçük bir üst simge referansı yerleştirecektir
// referans verdiği metnin sonrasını işaretle ve sayfanın alt kısmındaki ana gövde metninin altında bir giriş oluştur.
// Bu giriş dipnotun referans işaretini ve referans metnini içerecektir.
// bunu belge oluşturucunun "InsertFootnote" metoduna geçireceğiz.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Bu özellik "true" olarak ayarlanırsa, dipnotumuzun referans işareti
// bölümün tüm dipnotları arasında dizini olacaktır.
// Bu ilk dipnot olduğu için referans işareti "1" olacaktır.
Assert.True(footnote.IsAuto);

 // Belge oluşturucuyu dipnotun içine taşıyarak referans metnini düzenleyebiliriz.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti belirleyebiliriz.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// "IsAuto" bayrağı true olarak ayarlanmış bir yer imi hala gerçek dizinini gösterecektir
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
