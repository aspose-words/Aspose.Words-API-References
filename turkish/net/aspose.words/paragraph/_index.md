---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: .NET için Aspose.Words
description: Metin paragraflarını zahmetsizce yönetmek ve biçimlendirmek, belge işleme yeteneklerinizi geliştirmek için Aspose.Words.Paragraph sınıfını keşfedin.
type: docs
weight: 5120
url: /tr/net/aspose.words/paragraph/
---
## Paragraph class

Bir paragraf metni temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Paragraflarla Çalışma](https://docs.aspose.com/words/net/working-with-paragraphs/) belgeleme makalesi.

```csharp
public class Paragraph : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | Yeni bir örneğini başlatır`Paragraph` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Bu paragraf sonu bir Stil Ayırıcısıysa Doğru. Bir stil ayırıcısı, bir paragrafının farklı paragraf stillerine sahip parçalardan oluşmasına izin verir. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Çerçeve biçimlendirme özelliklerine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Bu paragraf bir paragrafın son paragrafıysa doğrudur[`Cell`](../../aspose.words.tables/cell/) ; aksi takdirde yanlış. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Bu paragraf belgenin son bölümündeki son paragraf ise doğrudur. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Bu paragraf, paragrafın son paragrafıysa doğrudur.[`HeaderFooter`](../headerfooter/) (ana metin hikayesi)[`Section`](../section/) ; aksi takdirde yanlış. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Bu paragraf, paragrafın son paragrafıysa doğrudur.[`Body`](../body/) (ana metin hikayesi)[`Section`](../section/) ; aksi takdirde yanlış. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Değişiklik izleme etkinleştirilmişken Microsoft Word'de nesnenin biçimlendirmesinin değiştirilmesi durumunda doğru değerini döndürür. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Bu paragrafın doğrudan bir alt paragrafı olması durumunda doğrudur[`Cell`](../../aspose.words.tables/cell/) ; aksi takdirde yanlış. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Paragraf orijinal revizyonda madde işaretli veya numaralı bir listede yer aldığında doğrudur. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse). |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse). |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Paragrafın liste biçimlendirme özelliklerine erişim sağlar. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Bir tane alır[`ListLabel`](./listlabel/)Bu paragraf için liste numaralandırma değerine ve biçimlendirmeye erişim sağlayan nesne |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | Geri DöndürürParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Paragraf sonu karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Paragraf biçimlendirme özelliklerine erişim sağlar. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Üst öğeyi alır[`Section`](../section/) paragrafın. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Ana bölüm düzeyindeki hikayeyi alır.[`Body`](../body/) veya[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Paragrafın içindeki metin parçalarının yazılmış koleksiyonuna erişim sağlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Belgenin paragrafının sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Belgenin paragrafının başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Bu paragrafa bir alan ekler. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Bu paragrafa bir alan ekler. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Bu paragrafa bir alan ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür; buna stiller veya listeler tarafından dolaylı olarak uygulananlar da dahildir. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Paragraf sonu karakteri dahil olmak üzere bu paragrafın metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Bu paragrafa bir alan ekler. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Bu paragrafa bir alan ekler. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Bu paragrafa bir alan ekler. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Paragraftaki aynı biçimlendirmeyle koşuları birleştirir. |
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

`Paragraph` blok düzeyinde bir düğümdür ve 'den türetilen sınıfların bir çocuğu olabilir[`Story`](../story/) veya[`InlineStory`](../inlinestory/).

`Paragraph` herhangi sayıda satır içi düzey düğüm ve yer imi içerebilir.

Bir paragrafın içinde bulunabilecek alt düğümlerin tam listesi şundan oluşur: [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Microsoft Word'de geçerli bir paragraf her zaman bir paragraf sonu karakteriyle biter ve asgari geçerli bir paragraf sadece bir paragraf sonundan oluşur.`Paragraph` sınıfı otomatik olarak uygun paragraf sonu karakterini sonuna ekler ve bu karakter alt düğümlerin bir parçası değildir`Paragraph` , bu nedenle a`Paragraph` boş olabilir.

Paragrafın sonunu dahil etmeyin[`ParagraphBreak`](../controlchar/paragraphbreak/) veya hücrenin sonu[`Cell`](../controlchar/cell/) Paragrafın metni içindeki karakterlerin olmaması, belge Microsoft Word'de açıldığında paragrafın geçersiz olmasına neden olabilir.

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
