---
title: Footnote Class
linktitle: Footnote
articleTitle: Footnote
second_title: .NET için Aspose.Words
description: Belgelerinizdeki dipnotları ve son notları kolay ve hassas bir şekilde yönetmek için temel aracınız olan Aspose.Words.Notes.Footnote sınıfını keşfedin.
type: docs
weight: 4950
url: /tr/net/aspose.words.notes/footnote/
---
## Footnote class

Bir dipnot veya sonnotun metni için bir kapsayıcıyı temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dipnot ve Sonnot ile Çalışma](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) belgeleme makalesi.

```csharp
public class Footnote : InlineStory
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Footnote](footnote/)(*[DocumentBase](../../aspose.words/documentbase/), [FootnoteType](../footnotetype/)*) | Bir örneğini başlatır`Footnote` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ActualReferenceMark](../../aspose.words.notes/footnote/actualreferencemark/) { get; } | Bu dipnot için belgede görüntülenen referans işaretinin gerçek metnini alır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Hikayedeki ilk paragrafı alır. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bu nesnenin bağlantı karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | Bunun bir dipnot mu yoksa sonnot mu olduğunu belirten bir değer döndürür. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | Bunun otomatik numaralandırılmış bir dipnot mu yoksa kullanıcı tanımlı özel referans işareti olan bir dipnot mu olduğunu belirten bir değeri tutar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse). |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse). |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Hikayedeki son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | Geri DöndürürFootnote . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Hikayenin doğrudan alt öğeleri olan paragrafların bir koleksiyonunu alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değer**boş dize** (Empty ), otomatik numaralı dipnotların kullanıldığı anlamına gelir. |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | Geri DöndürürFootnotes veyaEndnotes . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Hikayenin doğrudan alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words.notes/footnote/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Dipnotun sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words.notes/footnote/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Dipnotun başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
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

The`Footnote` sınıfı, bir Word belgesinde hem dipnotları hem de sonnotları temsil etmek için kullanılır.

`Footnote` satır içi düzeyde bir düğümdür ve yalnızca bir alt düğüm olabilir[`Paragraph`](../../aspose.words/paragraph/).

`Footnote` içerebilir[`Paragraph`](../../aspose.words/paragraph/) Ve[`Table`](../../aspose.words.tables/table/) çocuk düğümleri.

## Örnekler

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

* class [InlineStory](../../aspose.words/inlinestory/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
