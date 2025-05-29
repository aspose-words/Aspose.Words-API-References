---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: .NET için Aspose.Words
description: Bireysel belge bölümlerini zahmetsizce yönetmenin anahtarı olan Aspose.Words.Section sınıfını keşfedin. Belge düzenleme deneyiminizi bugün geliştirin!
type: docs
weight: 6560
url: /tr/net/aspose.words/section/
---
## Section class

Bir belgedeki tek bir bölümü temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bölümlerle Çalışma](https://docs.aspose.com/words/net/working-with-sections/) belgeleme makalesi.

```csharp
public sealed class Section : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | Section sınıfının yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | şunu döndürür:[`Body`](../body/) bölümün alt düğümü. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Bölümün başlık ve altbilgi düğümlerine erişim sağlar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | Geri DöndürürSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Sayfa düzenini ve bölüm özelliklerini temsil eden bir nesne döndürür. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Bölüm formlar için korunuyorsa doğrudur. Bir bölüm formlar için korunduğunda, kullanıcılar yalnızca Microsoft Word'deki form alanlarındaki metni seçebilir ve değiştirebilir. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words/section/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| override [AcceptStart](../../aspose.words/section/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | Bu bölümün sonuna kaynak bölümün içeriğinin bir kopyasını ekler. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Bölümü temizler. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/#clearheadersfooters)() | Bu bölümün başlıklarını ve altbilgilerini temizler. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/#clearheadersfooters_1)(*bool*) | Bu bölümün başlıklarını ve altbilgilerini temizler. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Bu bölümün bir kopyasını oluşturur. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Bu bölümün başlık ve altbilgilerinden tüm şekilleri (çizim nesnelerini) siler. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Bölümün şu şekilde olmasını sağlar:[`Body`](./body/) bir tanesiyle[`Paragraph`](../paragraph/) . |
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
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | Bu bölümün başına kaynak bölümün içeriğinin bir kopyasını ekler. |
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

`Section` bir tane olabilir[`Body`](../body/) ve en fazla bir tane[`HeaderFooter`](../headerfooter/) Her birinden [`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) Ve[`HeaderFooter`](../headerfooter/) nodes herhangi bir sırada olabilir`Section`.

Minimum geçerli bir bölümün şunlara sahip olması gerekir:[`Body`](../body/) bir tanesiyle[`Paragraph`](../paragraph/).

Her bölümün sayfa boyutu, yönlendirme, kenar boşlukları vb. gibi özellikleri belirten kendine özgü bir dizi özelliği vardır.

Bir bölümün kopyasını kullanarak oluşturabilirsiniz.[`Clone`](../node/clone/)Kopya aynı veya farklı bir belgeye eklenebilir.

Bölüm sonu ve bölüm özellikleri dahil olmak üzere tüm bir bölümü eklemek, eklemek veya kaldırmak için yöntemleri kullanın[`Sections`](../document/sections/) nesne.

Sadece bölüm içeriğini kopyalamak ve eklemek için, break ve bölüm özelliklerini kullanın[`AppendContent`](./appendcontent/) Ve[`PrependContent`](./prependcontent/) Yöntemler.

## Örnekler

Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümüyle sonuçlanır.
doc.RemoveAllChildren();

// Bu belgenin artık içerik ekleyebileceğimiz bileşik alt düğümleri yok.
// Düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecektir.
// İlk önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne bir alt bölüm olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa düzeni özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün, tüm içeriklerini barındıracak ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluştur, bazı biçimlendirme özelliklerini ayarla ve sonra onu gövdeye bir alt paragraf olarak ekle.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak, belgeyi yapmak için biraz içerik ekleyin. Bir çalışma oluşturun,
// Görünümünü ve içeriğini ayarlayın ve ardından paragrafın bir alt öğesi olarak ekleyin.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Ayrıca bakınız

* class [CompositeNode](../compositenode/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
