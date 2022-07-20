---
title: HeaderFooter
second_title: Aspose.Words for .NET API Referansı
description: Bir bölümün üstbilgi veya altbilgi metni için bir kapsayıcıyı temsil eder.
type: docs
weight: 2920
url: /tr/net/aspose.words/headerfooter/
---
## HeaderFooter class

Bir bölümün üstbilgi veya altbilgi metni için bir kapsayıcıyı temsil eder.

```csharp
public class HeaderFooter : Story
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HeaderFooter](headerfooter)(DocumentBase, HeaderFooterType) | Belirtilen türde yeni bir üstbilgi veya altbilgi oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Düğümün ilk alt öğesini alır. |
| [FirstParagraph](../../aspose.words/story/firstparagraph) { get; } | Öyküdeki ilk paragrafı alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype) { get; } | Bu üstbilgi/altbilginin türünü alır. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [IsHeader](../../aspose.words/headerfooter/isheader) { get; } | Bu doğruysa **Üstbilgi Altbilgi** nesne bir başlıktır. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious) { get; set; } | Bu üstbilgi veya altbilgi, önceki bölümdeki ilgili üstbilgi veya altbilgi ile bağlantılıysa doğrudur. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Düğümün son alt öğesini alır. |
| [LastParagraph](../../aspose.words/story/lastparagraph) { get; } | Öyküdeki son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/headerfooter/nodetype) { get; } | İade **NodeType.HeaderFooter** . |
| [Paragraphs](../../aspose.words/story/paragraphs) { get; } | Öykünün doğrudan alt öğeleri olan bir paragraf koleksiyonu alır. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentSection](../../aspose.words/headerfooter/parentsection) { get; } | Bu hikayenin üst bölümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [StoryType](../../aspose.words/story/storytype) { get; } | Bu hikayenin türünü alır. |
| [Tables](../../aspose.words/story/tables) { get; } | Öykünün doğrudan alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AppendParagraph](../../aspose.words/story/appendparagraph)(string) | Bir[`Paragraph`](../paragraph) isteğe bağlı metin içeren nesne ve onu bu nesnenin sonuna ekler. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [DeleteShapes](../../aspose.words/story/deleteshapes)() | Bu hikayenin metninden tüm şekilleri siler. |
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

**Üstbilgi Altbilgi** içerebilir **Paragraf** ve **Masa** alt düğümler.

**Üstbilgi Altbilgi** bölüm düzeyinde bir düğümdür ve yalnızca alt öğesi olabilir **Bölüm** . Yalnızca bir tane olabilir **Üstbilgi Altbilgi** veya her biri[`HeaderFooterType`](./headerfootertype) içinde **Bölüm**.

Eğer **Bölüm** sahip değil **Üstbilgi Altbilgi** belirli bir türün or  **Üstbilgi Altbilgi** alt düğümü yok, bu üstbilgi/altbilgi, Microsoft Word'deki önceki bölümün aynı türdeki üstbilgi/altbilgisine bağlı olarak kabul edilir.

Ne zaman **Üstbilgi Altbilgi** en az bir tane içerir **Paragraf**, artık Microsoft Word'de öncekiyle bağlantılı olarak kabul edilmez.

### Örnekler

Belgenin alt bilgisindeki metnin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Bir belgeden tüm alt bilgilerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Her bölümü yineleyin ve her türden altbilgiyi kaldırın.
foreach (Section section in doc.OfType<Section>())
{
    //Üç çeşit altbilgi ve üstbilgi türü vardır.
    // 1 - Bir bölümün yalnızca ilk sayfasında görünen "İlk" üstbilgi/altbilgi.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Tek sayfalarda görünen "Birincil" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Çift sayfalarda görünen "Eşit" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Üstbilgi ve altbilginin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Bir başlık oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının başında, ana gövde metninin üstünde görünecektir.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Bir alt bilgi oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının altında, ana gövde metninin altında görünecektir.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Ayrıca bakınız

* class [Story](../story)
* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
