---
title: InlineStory
second_title: Aspose.Words for .NET API Referansı
description: Paragraflar ve tablolar içerebilen satır içi düzey düğümler için temel sınıf.
type: docs
weight: 3070
url: /tr/net/aspose.words/inlinestory/
---
## InlineStory class

Paragraflar ve tablolar içerebilen satır içi düzey düğümler için temel sınıf.

```csharp
public abstract class InlineStory : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Düğümün ilk alt öğesini alır. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Öyküdeki ilk paragrafı alır. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Bu nesnenin bağlantı karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Düğümün son alt öğesini alır. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Öyküdeki son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Bu düğümün türünü alır. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Öykünün doğrudan alt öğeleri olan bir paragraf koleksiyonu alır. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype) { get; } | Öykünün türünü döndürür. |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Öykünün doğrudan alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Son alt öğe bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

**satır içi hikaye** blok düzeyinde düğümler için bir kapsayıcıdır[`Paragraph`](../paragraph) ve[`Table`](../../aspose.words.tables/table).

Kaynaklanan sınıflar **satır içi hikaye** kendi metinlerini (paragraflar ve tablolar) içerebilen satır içi düzey düğümlerdir. Örneğin, bir **Yorum** düğüm, bir comment metni ve bir **Dipnot** dipnot metni içerir.

### Örnekler

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

// Microsoft Word'de, düzenlemek veya yanıtlamak için belge gövdesindeki bu yorumu sağ tıklatabiliriz. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Dipnotların nasıl ekleneceğini ve özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metin ekleyin ve bir dipnotla referans verin. Bu dipnot küçük bir üst simge referansı yerleştirecektir
// referans verdiği metinden sonra işaretleyin ve sayfanın altındaki ana gövde metninin altında bir giriş oluşturun.
// Bu giriş, dipnotun referans işaretini ve referans metnini içerecektir,
// belge oluşturucunun "InsertFootnote" yöntemine geçeceğiz.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Bu özellik "true" olarak ayarlanırsa dipnotumuzun referans işareti
// tüm bölümün dipnotları arasında indeksi olacaktır.
// Bu ilk dipnottur, dolayısıyla referans işareti "1" olacaktır.
Assert.True(footnote.IsAuto);

// Referans metnini düzenlemek için belge oluşturucuyu dipnotun içine taşıyabiliriz. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti belirleyebiliriz.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// "IsAuto" bayrağı true olarak ayarlanmış bir yer imi gerçek dizinini göstermeye devam edecek
// önceki yer imleri özel referans işaretleri gösterse bile, bu nedenle bu yer iminin referans işareti "3" olacaktır.
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Ayrıca bakınız

* class [CompositeNode](../compositenode)
* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
