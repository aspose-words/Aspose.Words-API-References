---
title: "Aspose::Words::Paragraph sınıfı"
linktitle: "Paragraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph sınıfı. Metin paragrafını temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 47000
url: /tr/cpp/aspose.words/paragraph/
---
## Paragraph class


Metin paragrafını temsil eder. Daha fazla bilgi edinmek için, [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) dokümantasyon makalesini ziyaret edin.

```cpp
class Paragraph : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IParaAttrSource,
                  public Aspose::Words::IRunAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Belgenin paragrafının sonunu ziyaret etmek için bir ziyaretçi kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Belgenin paragrafının başlangıcını ziyaret etmek için bir ziyaretçi kabul eder. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendField](./appendfield/)(Aspose::Words::Fields::FieldType, bool) | Bu paragrafa bir alan ekler. |
| [AppendField](./appendfield/)(const System::String\&) | Bu paragrafa bir alan ekler. |
| [AppendField](./appendfield/)(const System::String\&, const System::String\&) | Bu paragrafa bir alan ekler. |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_BreakIsStyleSeparator](./get_breakisstyleseparator/)() | Bu paragraf kesmesi bir [Style](../style/) Ayırıcıysa doğru. Bir stil ayırıcı, bir paragrafın farklı paragraf stillerine sahip bölümlerden oluşmasına izin verir. |
| [get_Count](../compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FrameFormat](./get_frameformat/)() | Çerçeve biçimlendirme özelliklerine erişim sağlar. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsEndOfCell](./get_isendofcell/)() | Bu paragraf bir [Cell](../../aspose.words.tables/cell/) içindeki son paragraf ise doğru; aksi takdirde yanlış. |
| [get_IsEndOfDocument](./get_isendofdocument/)() | Bu paragraf belgenin son bölümündeki son paragraf ise doğru. |
| [get_IsEndOfHeaderFooter](./get_isendofheaderfooter/)() | Bu paragraf bir [Section](../section/) içindeki [HeaderFooter](../headerfooter/) (ana metin hikayesi) içinde son paragraf ise doğru; aksi takdirde yanlış. |
| [get_IsEndOfSection](./get_isendofsection/)() | Bu paragraf bir [Section](../section/) içindeki [Body](../body/) (ana metin hikayesi) içinde son paragraf ise doğru; aksi takdirde yanlış. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Değişiklik izleme etkinleştirildiği sırada Microsoft Word'de nesnenin biçimlendirmesi değiştirildiyse true döndürür. |
| [get_IsInCell](./get_isincell/)() | Bu paragraf bir [Cell](../../aspose.words.tables/cell/) öğesinin doğrudan çocuğu ise doğru; aksi takdirde yanlış. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsListItem](./get_islistitem/)() | Paragraf orijinal revizyonda madde işaretli veya numaralı bir listede bir öğe olduğunda doğru. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_ListFormat](./get_listformat/)() | Paragrafın liste biçimlendirme özelliklerine erişim sağlar. |
| [get_ListLabel](./get_listlabel/)() | [ListLabel](./get_listlabel/) nesnesi alır; bu nesne bu paragraf için liste numaralandırma değeri ve biçimlendirmesine erişim sağlar. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | [Paragraph](../nodetype/) döndürür. |
| [get_ParagraphBreakFont](./get_paragraphbreakfont/)() | Paragraf sonu karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Paragraf biçimlendirme özelliklerine erişim sağlar. |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentSection](./get_parentsection/)() | Paragrafın üst [Section](../section/) öğesini alır. |
| [get_ParentStory](./get_parentstory/)() | Üst bölüm seviyesindeki hikâyeyi alır; bu hikâye [Body](../body/) ya da [HeaderFooter](../headerfooter/) olabilir. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [get_Runs](./get_runs/)() | Paragraf içindeki metin parçalarının tiplenmiş koleksiyonuna erişim sağlar. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../nodetype/) öğesinin ilk atasını alır. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEffectiveTabStops](./geteffectivetabstops/)() | Bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür; stil veya listeler tarafından dolaylı olarak uygulananlar da dahil. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](./gettext/)() override | Bu paragrafın metnini, paragraf sonu karakteri dahil olmak üzere alır. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Bu paragrafa bir alan ekler. |
| [InsertField](./insertfield/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Bu paragrafa bir alan ekler. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Bu paragrafa bir alan ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Paragrafta aynı biçimlendirmeye sahip koşuları birleştirir. |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) | Paragrafta aynı biçimlendirmeye sahip koşuları birleştirir. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [Paragraph](./paragraph/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | [Paragraph](./) sınıfının yeni bir örneğini başlatır. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../node/) öğesini seçer. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) için ayarlayıcı. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


[Paragraph](./) is a block-level node and can be a child of classes derived from [Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

Bir paragraf içinde oluşabilecek alt düğümlerin tam listesi şunları içerir: [BookmarkStart](../bookmarkstart/), [BookmarkEnd](../bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../run/), [SpecialChar](../specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [SmartTag](../../aspose.words.markup/smarttag/).

Microsoft Word'de geçerli bir paragraf her zaman bir paragraf sonu karakteriyle biter ve minimal geçerli bir paragraf sadece bir paragraf sonundan oluşur. [Paragraph](./) sınıfı otomatik olarak uygun paragraf sonu karakterini sona ekler ve bu karakter [Paragraph](./) alt düğümlerinin bir parçası değildir; bu nedenle bir [Paragraph](./) boş olabilir.

Paragrafın metni içinde paragraf sonu [ParagraphBreak](../controlchar/paragraphbreak/) veya hücre sonu [Cell](../controlchar/cell/) karakterlerini eklemeyin; aksi takdirde belge Microsoft Word'de açıldığında paragraf geçersiz olabilir.

## Örnekler



Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
// "RemoveAllChildren" yöntemini çağırarak bu düğümlerin tümünü kaldırın,
// ve hiçbir çocuğu olmayan bir belge düğümü elde edin.
doc->RemoveAllChildren();

// Bu belge artık içerik ekleyebileceğimiz birleşik alt düğümlere sahip değil.
// Eğer düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// İlk olarak yeni bir bölüm oluşturun ve ardından kök belge düğümüne çocuk olarak ekleyin.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Bölüm için bazı sayfa ayarı özelliklerini ayarlayın.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Bir bölüm bir gövdeye ihtiyaç duyar, bu gövde tüm içeriğini barındırır ve gösterir
// sayfada bölümün başlığı ile altbilgisi arasındaki alanda.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu gövdenin bir çocuğu olarak ekleyin.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Son olarak, belgeye içerik ekleyin. Bir run oluşturun,
// Görünümünü ve içeriğini ayarlayın, ardından onu paragrafın bir çocuğu olarak ekleyin.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Ayrıca Bakınız

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
