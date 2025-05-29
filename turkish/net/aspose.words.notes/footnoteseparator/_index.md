---
title: FootnoteSeparator Class
linktitle: FootnoteSeparator
articleTitle: FootnoteSeparator
second_title: .NET için Aspose.Words
description: Herhangi bir belgede dipnot ve sonnot içeriğini sorunsuz bir şekilde yönetmenin anahtarı olan Aspose.Words.Notes.FootnoteSeparator sınıfını keşfedin.
type: docs
weight: 4990
url: /tr/net/aspose.words.notes/footnoteseparator/
---
## FootnoteSeparator class

Bir belgenin dipnot/sonnot ayırıcısı ve devam içeriği için bir kapsayıcıyı temsil eder.

```csharp
public class FootnoteSeparator : Story
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Hikayedeki ilk paragrafı alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Hikayedeki son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.notes/footnoteseparator/nodetype/) { get; } |  |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Hikayenin doğrudan alt öğeleri olan paragrafların bir koleksiyonunu alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [SeparatorType](../../aspose.words.notes/footnoteseparator/separatortype/) { get; } |  |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Bu hikayenin türünü alır. |
| [Tables](../../aspose.words/story/tables/) { get; } | Hikayenin doğrudan alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnoteseparator/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) |  |
| override [AcceptEnd](../../aspose.words.notes/footnoteseparator/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) |  |
| override [AcceptStart](../../aspose.words.notes/footnoteseparator/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | Bir kısayol yöntemi oluşturan[`Paragraph`](../../aspose.words/paragraph/) isteğe bağlı metin içeren nesne ve bu nesnenin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Bu hikayenin metninden tüm şekilleri siler. |
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

`FootnoteSeparator` içerebilir[`Paragraph`](../../aspose.words/paragraph/) Ve[`Masa`](../../aspose.words.tables/table/) çocuk düğümleri.

Sadece bir tane olabilir`FootnoteSeparator` her birinin[`FootnoteSeparatorType`](../footnoteseparatortype/) Bir belgede.

## Örnekler

Dipnot ayırıcı formatının nasıl yönetileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Dipnot ayırıcısını hizala.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Ayrıca bakınız

* class [Story](../../aspose.words/story/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
