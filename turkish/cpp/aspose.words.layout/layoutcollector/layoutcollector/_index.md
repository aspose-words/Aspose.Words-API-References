---
title: "Aspose::Words::Layout::LayoutCollector::LayoutCollector yapıcı"
linktitle: "LayoutCollector"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutCollector::LayoutCollector yapıcı. C++'da bu sınıfın bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.layout/layoutcollector/layoutcollector/
---
## LayoutCollector::LayoutCollector constructor


Bu sınıfın bir örneğini başlatır.

```cpp
Aspose::Words::Layout::LayoutCollector::LayoutCollector(const System::SharedPtr<Aspose::Words::Document> &doc)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::Document\>\& | Bu toplama örneğinin ilişkilendirileceği belge. |

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

* Class [Document](../../../aspose.words/document/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
