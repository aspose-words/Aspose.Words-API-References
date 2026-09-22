---
title: "Aspose::Words::Layout::LayoutCollector::GetEntity yöntemi"
linktitle: "GetEntity"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutCollector::GetEntity yöntemi. Belirtilen düğüme karşılık gelen LayoutEnumerator'ın opak bir konumunu döndürür. Sayılamakta olan belge ile düğümün belgesi aynı olduğunda döndürülen değeri Current yöntemine argüman olarak kullanabilirsiniz."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


Belirtilen düğüme karşılık gelen [LayoutEnumerator](../../layoutenumerator/) opak bir konum döndürür. Sayılamakta olan belge ile düğümün belgesi aynı olduğunda döndürülen değeri [Current](../../layoutenumerator/get_current/) yöntemine argüman olarak kullanabilirsiniz.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## Açıklamalar


Bu yöntem yalnızca [Paragraph](../../../aspose.words/paragraph/) düğümleri ve bölünemez satır içi düğümler, ör. [BookmarkStart](../../../aspose.words/bookmarkstart/) veya [Shape](../../../aspose.words.drawing/shape/) için çalışır. [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) veya [Table](../../../aspose.words.tables/table/) düğümleri ve başlık/altbilgi içindeki düğümler için çalışmaz.

Bir [Paragraph](../../../aspose.words/paragraph/) düğümü için döndürülen varlığın bir paragraf kesme aralığı olduğunu unutmayın. Üst satıra yükselmek için uygun yöntemi kullanın.

Bir metin [Run](../../../aspose.words/run/) öğesine gitmeniz gerekiyorsa, önüne bir yer imi ekleyebilir ve ardından yer imine yönlendirebilirsiniz.

Bir [Cell](../../../aspose.words.tables/cell/) düğümüne gitmeniz gerekiyorsa, bu hücredeki bir [Paragraph](../../../aspose.words/paragraph/) düğümüne geçebilir ve ardından üst varlığa yükseltebilirsiniz. Aynı yaklaşım [Row](../../../aspose.words.tables/row/) ve [Table](../../../aspose.words.tables/table/) düğümleri için de kullanılabilir.

## Örnekler



Bir düğümün kapsadığı sayfa aralıklarını nasıl göreceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// "GetNumPagesSpanned" yöntemini çağırarak belgemizin içeriğinin kaç sayfa kapsadığını sayın.
// Belge boş olduğundan, sayfa sayısı şu anda sıfırdır.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Belgeyi 5 sayfa içerikle doldurun.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Yerleşim toplayıcısından önce, bize vermesi için "UpdatePageLayout" yöntemini çağırmamız gerekir
// sayfa sayısı gibi herhangi bir yerleşimle ilgili ölçüm için doğru bir rakam.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// Herhangi bir düğümün başlangıç ve bitiş sayfa numaralarını ve bunların toplam sayfa aralıklarını görebiliriz.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// LayoutEnumerator kullanarak yerleşim varlıkları üzerinde yineleyebiliriz.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// LayoutEnumerator, yerleşim varlıkları koleksiyonunu bir ağaç gibi gezebilir.
// Bunu ayrıca herhangi bir düğümün ilgili yerleşim varlığına uygulayabiliriz.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## Ayrıca Bakınız

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
