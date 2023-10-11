---
title: Class Paragraph
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Paragraph sınıf. Metnin bir paragrafını temsil eder.
type: docs
weight: 4390
url: /tr/net/aspose.words/paragraph/
---
## Paragraph class

Metnin bir paragrafını temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Paragraflarla Çalışmak](https://docs.aspose.com/words/net/working-with-paragraphs/) dokümantasyon makalesi.

```csharp
public class Paragraph : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Paragraph](paragraph/)(DocumentBase) | Yeni bir örneğini başlatır`Paragraph` class. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Bu paragraf sonu bir Stil Ayırıcı ise doğrudur. Stil ayırıcı, one paragrafının farklı paragraf stillerine sahip parçalardan oluşmasına olanak tanır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Çerçeve biçimlendirme özelliklerine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | İadeler`doğru` bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | İadeler`doğru` çünkü bu düğüm alt düğümlere sahip olabilir. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true değerini döndürür. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Bu paragraf bir paragraftaki son paragrafsa doğrudur[`Cell`](../../aspose.words.tables/cell/) ; aksi halde yanlış. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Bu paragraf belgenin son bölümünün son paragrafı ise doğrudur. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Bu paragraf paragraftaki son paragrafsa doğru[`HeaderFooter`](../headerfooter/) (ana metin hikayesi) bir[`Section`](../section/) ; aksi halde yanlış. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Bu paragraf paragraftaki son paragrafsa doğru[`Body`](../body/) (ana metin hikayesi) bir[`Section`](../section/) ; aksi halde yanlış. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Microsoft Word'de değişiklik izleme etkinken nesnenin biçimlendirmesi değiştirilmişse doğru değerini döndürür. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Bu paragrafın doğrudan alt öğesi ise doğrudur[`Cell`](../../aspose.words.tables/cell/) ; aksi halde yanlış. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Paragrafın orijinal revizyondaki madde işaretli veya numaralı listedeki bir öğe olması durumunda doğrudur. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | İadeler`doğru` değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse). |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Paragrafın liste biçimlendirme özelliklerine erişim sağlar. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Bir alır[`ListLabel`](./listlabel/)bu paragraf için liste numaralandırma değerine ve formatlama 'ye erişim sağlayan nesne. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | İadelerParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Paragraf sonu karakterinin yazı tipi formatına erişim sağlar. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Paragraf biçimlendirme özelliklerine erişim sağlar. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Üst öğeyi alır[`Section`](../section/) paragrafın. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Oluşturulabilecek ana bölüm düzeyindeki öyküyü alır.[`Body`](../body/) veya[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Paragrafın içinde yazılan metin parçaları koleksiyonuna erişim sağlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(DocumentVisitor) | Ziyaretçi kabul eder. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(string) | Bu paragrafa bir alan ekler. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(FieldType, bool) | Bu paragrafa bir alan ekler. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(string, string) | Bu paragrafa bir alan ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atayı alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Stiller veya listeler tarafından dolaylı olarak uygulananlar da dahil olmak üzere, bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Paragraf sonu karakteri de dahil olmak üzere bu paragrafın metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisinde belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(string, Node, bool) | Bu paragrafa bir alan ekler. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(FieldType, bool, Node, bool) | Bu paragrafa bir alan ekler. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(string, string, Node, bool) | Bu paragrafa bir alan ekler. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Birleştirmeler paragrafta aynı biçimlendirmeyle çalışır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
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

`Paragraph` blok düzeyinde bir düğümdür ve from 'den türetilen sınıfların çocuğu olabilir[`Story`](../story/) veya[`InlineStory`](../inlinestory/).

`Paragraph` herhangi bir sayıda satır içi düzey düğümü ve yer imini içerebilir.

Bir paragrafın içinde oluşabilecek alt düğümlerin tam listesi şunlardan oluşur: [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Microsoft Word'deki geçerli bir paragraf her zaman paragraf sonu karakteriyle biter ve minimum geçerli paragraf yalnızca paragraf sonundan oluşur.`Paragraph` sınıfı uygun paragraf sonu karakterini end sonuna otomatik olarak ekler ve bu karakter, sınıfın alt düğümlerinin bir parçası değildir.`Paragraph` , dolayısıyla a`Paragraph` boş olabilir.

Paragrafın sonunu eklemeyin[`ParagraphBreak`](../controlchar/paragraphbreak/) veya hücrenin sonu[`Cell`](../controlchar/cell/) Belge Microsoft Word'de açıldığında paragrafın geçersiz olmasına neden olabileceği için paragrafın metninin içindeki karakterleri.

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


