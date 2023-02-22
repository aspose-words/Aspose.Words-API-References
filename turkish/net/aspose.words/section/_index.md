---
title: Class Section
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Section sınıf. Belgedeki tek bir bölümü temsil eder.
type: docs
weight: 5440
url: /tr/net/aspose.words/section/
---
## Section class

Belgedeki tek bir bölümü temsil eder.

```csharp
public sealed class Section : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Section](section/)(DocumentBase) | Section sınıfının yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | **Gövde** bölümün alt düğümü. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk alt öğesini alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Bölümün üstbilgi ve altbilgi düğümlerine erişim sağlar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son alt öğesini alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | İade **DüğümTürü.Bölüm** . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Sayfa düzenini ve bölüm özelliklerini temsil eden bir nesne döndürür. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Bölüm formlar için korunuyorsa doğrudur. Bir bölüm formlar için korunduğunda, kullanıcıları yalnızca Microsoft Word'deki form alanlarındaki metni seçebilir ve değiştirebilir. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AppendContent](../../aspose.words/section/appendcontent/)(Section) | Bu bölümün sonuna kaynak bölümün içeriğinin bir kopyasını ekler. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Bölümü temizler. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Bu bölümün üstbilgilerini ve altbilgilerini temizler. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Bu bölümün bir kopyasını oluşturur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Bu bölümün üstbilgilerinden ve altbilgilerinden tüm şekilleri (çizim nesneleri) siler. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Bölümün bir Paragraflı Gövdeye sahip olmasını sağlar. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PrependContent](../../aspose.words/section/prependcontent/)(Section) | Bu bölümün başına kaynak bölümün içeriğinin bir kopyasını ekler. |
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

**Bölüm** bir tane olabilir[`Body`](./body/) ve maksimum bir[`HeaderFooter`](../headerfooter/) her birinin [`HeaderFooterType`](../headerfootertype/) . **Gövde** ve **Üstbilgi Altbilgi** Nodes içinde herhangi bir sırada olabilir **Bölüm**.

Minimum geçerli bir bölümün olması gerekir **Gövde** biriyle **Paragraf**.

Her bölümün sayfa boyutunu, yönünü, kenar boşluklarını vb. belirten kendi özellikleri vardır.

kullanarak bir bölümün bir kopyasını oluşturabilirsiniz.[`Clone`](../node/clone/). Kopya, aynı veya farklı belgeye eklenebilir.

Bölüm sonu ve bölüm özellikleri dahil olmak üzere bir bölümün tamamını eklemek, eklemek veya kaldırmak için aşağıdaki yöntemleri kullanın: **Bölümler** nesne.

Break bölümü ve bölüm özellikleri hariç sadece bölümün içeriğini kopyalamak ve eklemek için **İçerik Ekle** ve **Başa Ekleİçerik**yöntemler.

### Örnekler

Bir Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve alt öğesi olmayan bir belge düğümüyle bitirin.
doc.RemoveAllChildren();

// Bu belgede artık içerik ekleyebileceğimiz bileşik alt düğüm yok.
// Düzenlemek istiyorsak, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// Önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne alt öğe olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa kurulum özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün tüm içeriğini içerecek ve görüntüleyecek bir gövdeye ihtiyacı var
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu alt öğe olarak gövdeye ekleyin.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak, belgeyi yapmak için biraz içerik ekleyin. Bir koşu oluşturun,
// görünümünü ve içeriğini ayarlayın ve ardından paragrafa alt öğe olarak ekleyin.
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


