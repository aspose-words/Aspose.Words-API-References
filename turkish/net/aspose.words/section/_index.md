---
title: Class Section
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Section sınıf. Bir belgedeki tek bir bölümü temsil eder.
type: docs
weight: 5730
url: /tr/net/aspose.words/section/
---
## Section class

Bir belgedeki tek bir bölümü temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bölümlerle Çalışmak](https://docs.aspose.com/words/net/working-with-sections/) dokümantasyon makalesi.

```csharp
public sealed class Section : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Section](section/)(DocumentBase) | Bölüm sınıfının yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Şunu döndürür:[`Body`](../body/) bölümün alt düğümü. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | İadeler`doğru` bu düğümün herhangi bir alt düğümü varsa. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Bölümün üst bilgi ve alt bilgi düğümlerine erişim sağlar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | İadeler`doğru` çünkü bu düğüm alt düğümlere sahip olabilir. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | İadelerSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Sayfa düzenini ve bölüm özelliklerini temsil eden bir nesneyi döndürür. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Bölüm formlar için korunuyorsa doğrudur. Bir bölüm formlar için korunduğunda, kullanıcıları yalnızca Microsoft Word'deki form alanlarındaki metni seçebilir ve değiştirebilir. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(DocumentVisitor) | Ziyaretçi kabul eder. |
| override [AcceptEnd](../../aspose.words/section/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/section/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendContent](../../aspose.words/section/appendcontent/)(Section) | Kaynak bölümünün içeriğinin bir kopyasını bu bölümün sonuna ekler. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Bölümü temizler. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Bu bölümün üstbilgilerini ve altbilgilerini temizler. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Bu bölümün bir kopyasını oluşturur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Bu bölümün üst bilgilerinden ve alt bilgilerinden tüm şekilleri (çizim nesneleri) siler. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Bölümün sahip olmasını sağlar[`Body`](./body/) biriyle[`Paragraph`](../paragraph/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atayı alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisinde belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PrependContent](../../aspose.words/section/prependcontent/)(Section) | Kaynak bölümünün içeriğinin bir kopyasını bu bölümün başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/)Geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | İlkini seçer[`Node`](../node/) XPath ifadesiyle eşleşen. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

`Section` bir tane olabilir[`Body`](../body/) ve maksimum bir[`HeaderFooter`](../headerfooter/) her birinden [`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) Ve[`HeaderFooter`](../headerfooter/) nodes içeride herhangi bir sırada olabilir`Section`.

Minimum geçerli bölümün olması gerekir[`Body`](../body/) biriyle[`Paragraph`](../paragraph/).

Her bölümün sayfa boyutunu, yönünü, kenar boşluklarını vb. belirten kendi özellikleri vardır.

kullanarak bir bölümün kopyasını oluşturabilirsiniz.[`Clone`](../node/clone/). Kopya aynı veya farklı belgeye eklenebilir.

Bölüm sonu ve bölüm özellikleri de dahil olmak üzere bir bölümün tamamını eklemek, eklemek veya kaldırmak için aşağıdaki yöntemleri kullanın:[`Sections`](../document/sections/) nesne.

Break bölümü ve bölüm özellikleri hariç, yalnızca bölümün içeriğini kopyalamak ve eklemek için şunu kullanın:[`AppendContent`](./appendcontent/) Ve[`PrependContent`](./prependcontent/) yöntemler.

### Örnekler

Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümü elde ederiz.
doc.RemoveAllChildren();

// Bu belgede artık içerik ekleyebileceğimiz bileşik alt düğüm yok.
// Eğer onu düzenlemek istiyorsak, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// Öncelikle yeni bir bölüm oluşturun ve ardından bunu alt öğe olarak kök belge düğümüne ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa yapısı özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün tüm içeriğini içerecek ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu alt öğe olarak gövdeye ekleyin.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak belgeyi yapmak için biraz içerik ekleyin. Bir koşu oluşturun,
// görünüşünü ve içeriğini ayarlayın ve ardından onu alt öğe olarak paragrafa ekleyin.
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


