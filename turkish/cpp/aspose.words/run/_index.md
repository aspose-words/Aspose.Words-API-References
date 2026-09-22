---
title: "Aspose::Words::Run class"
linktitle: "Run"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Run class. Aynı yazı tipi biçimlendirmesine sahip karakterlerin bir koşusunu temsil eder. Daha fazla bilgi için C++'deki belge makalesini ziyaret edin."
type: docs
weight: 56000
url: /tr/cpp/aspose.words/run/
---
## Run class


Aynı yazı tipi biçimlendirmesine sahip karakterlerin bir koşusunu temsil eder. Daha fazla bilgi edinmek için, [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
class Run : public Aspose::Words::Inline
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_Font](../inline/get_font/)() | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | Değişiklik izleme etkinleştirildiği sırada Microsoft Word'de nesnenin biçimlendirmesi değiştirildiyse true döndürür. |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_IsPhoneticGuide](./get_isphoneticguide/)() | Koşunun fonetik bir kılavuz olup olmadığını gösteren bir boolean değer döndürür. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | Döndürür [Run](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | Bu düğümün üst [Paragraph](../paragraph/) öğesini alır. |
| [get_PhoneticGuide](./get_phoneticguide/)() | Bir [PhoneticGuide](./get_phoneticguide/) nesnesi alır. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [get_Text](./get_text/)() const | Koşunun metnini alır veya ayarlar. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../nodetype/) öğesinin ilk atasını alır. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Koşunun metnini alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../node/remove/)() | Kendisini üst düğümden kaldırır. |
| [Run](./run/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Yeni bir [Run](./) sınıf örneği başlatır. |
| [Run](./run/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Yeni bir **Run** sınıf örneği başlatır. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) için ayarlayıcı. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Text](./set_text/)(const System::String\&) | [Aspose::Words::Run::get_Text](./get_text/) için ayarlayıcı. |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Belgenin tüm metni run'lar içinde depolanır.

[Run](./) can only be a child of [Paragraph](../paragraph/) or inline [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).

## Örnekler



Bir metin run'ını font özelliğini kullanarak nasıl biçimlendireceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


Bir [CompositeNode](../compositenode/)'in çocuk koleksiyonunda alt düğümleri ekleme, güncelleme ve silme yollarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge, varsayılan olarak bir paragraf içerir.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Paragrafımız gibi birleşik düğümler, diğer birleşik ve satır içi düğümleri çocuk olarak içerebilir.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Üç tane daha run düğümü oluştur.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Belge gövdesi, bu run'ları bir birleşik düğüme ekleyene kadar göstermez
// ki kendisi belge düğüm ağacının bir parçasıdır, ilk run ile yaptığımız gibi.
// Eklediğimiz düğümlerin metin içeriklerinin nerede olduğunu belirleyebiliriz
// paragraftaki başka bir düğüme göre bir ekleme konumu belirterek belgedeki konumunu belirleyebiliriz.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// İkinci run'ı, ilk run'ın önüne paragrafta ekleyin.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Üçüncü run'ı, ilk run'dan sonra ekleyin.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// İlk run'ı, paragrafın çocuk düğüm koleksiyonunun başına ekleyin.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Mevcut çocuk düğümleri düzenleyerek ve silerek run'ın içeriğini değiştirebiliriz.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```


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

* Class [Inline](../inline/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
