---
title: Class Paragraph
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Paragraph sınıf. Bir metin paragrafını temsil eder.
type: docs
weight: 4150
url: /tr/net/aspose.words/paragraph/
---
## Paragraph class

Bir metin paragrafını temsil eder.

```csharp
public class Paragraph : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Paragraph](paragraph/)(DocumentBase) | Yeni bir örneğini başlatır **Paragraf** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Bu paragraf sonu bir Stil Ayırıcı ise doğrudur. Stil ayırıcı, one paragrafın farklı paragraf stillerine sahip parçalardan oluşmasına izin verir. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk alt öğesini alır. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Paragraf biçimlendirme özelliklerine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Bu paragraf bir metindeki son paragrafsa doğrudur[`Cell`](../../aspose.words.tables/cell/) ; aksi halde yanlış. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Bu paragraf belgenin son bölümündeki son paragrafsa doğrudur. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Bu paragraf metnin son paragrafıysa doğrudur **Üstbilgi Altbilgi** (ana metin hikayesi) bir **Bölüm** ; aksi halde yanlış. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Bu paragraf metnin son paragrafıysa doğrudur **Gövde** (ana metin hikayesi) bir **Bölüm** ; aksi halde yanlış. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilirse doğru döndürür. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Bu paragraf aşağıdaki öğenin hemen alt öğesiyse doğrudur[`Cell`](../../aspose.words.tables/cell/) ; aksi halde yanlış. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Paragraf, orijinal revizyondaki madde işaretli veya numaralı listedeki bir öğe olduğunda doğrudur. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son alt öğesini alır. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Paragrafın liste biçimlendirme özelliklerine erişim sağlar. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | [`ListLabel`](./listlabel/) bu paragraf için liste numaralandırma değerine ve biçimlendirmeye erişim sağlayan nesne . |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | İade **DüğümTürü.Paragraf** . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Paragraf sonu karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Paragraf biçimlendirme özelliklerine erişim sağlar. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Üst öğeyi alır[`Section`](../section/) paragrafın. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Olabilecek üst bölüm düzeyinde öyküyü alır.[`Body`](../body/) veya[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Paragraf içinde yazılan metin parçaları koleksiyonuna erişim sağlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(string) | Bu paragrafa bir alan ekler. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(FieldType, bool) | Bu paragrafa bir alan ekler. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(string, string) | Bu paragrafa bir alan ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Stiller veya listeler tarafından dolaylı olarak uygulananlar da dahil olmak üzere, bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Paragraf sonu karakteri dahil bu paragrafın metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(string, Node, bool) | Bu paragrafa bir alan ekler. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(FieldType, bool, Node, bool) | Bu paragrafa bir alan ekler. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(string, string, Node, bool) | Bu paragrafa bir alan ekler. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Paragraftaki aynı biçimlendirmeyle çalıştırmaları birleştirir. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
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

`Paragraph` blok düzeyinde bir düğümdür ve öğesinden türetilen sınıfların alt öğesi olabilir[`Story`](../story/) veya[`InlineStory`](../inlinestory/).

`Paragraph` herhangi bir sayıda satır içi düzey düğüm ve yer imi içerebilir.

Bir paragraf içinde oluşabilecek alt düğümlerin tam listesi, 'den oluşur.[`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Microsoft Word'de geçerli bir paragraf her zaman bir paragraf sonu karakteriyle biter ve en az geçerli paragraf yalnızca bir paragraf sonundan oluşur. bu **Paragraf** sınıfı, end sonuna uygun paragraf kesme karakterini otomatik olarak ekler ve bu karakter, dizinin alt düğümlerinin bir parçası değildir. **Paragraf** , bu nedenle a **Paragraf** boş olabilir.

Paragrafın sonunu eklemeyin[`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak/) veya hücrenin sonu[`KontrolChar.Hücresi`](../controlchar/cell/) Belge Microsoft Word'de açıldığında paragrafı geçersiz kılabileceğinden, paragrafın metni içindeki karakterler.

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


