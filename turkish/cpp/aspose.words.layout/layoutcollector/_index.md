---
title: "Aspose::Words::Layout::LayoutCollector sınıfı"
linktitle: "LayoutCollector"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutCollector sınıfı. Bu sınıf, belge düğümlerinin sayfa numaralarını hesaplamayı sağlar. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


Bu sınıf, belge düğümlerinin sayfa numaralarını hesaplamayı sağlar. Daha fazla bilgi için, [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin.

```cpp
class LayoutCollector : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clear](./clear/)() | Toplanan tüm yerleşim verilerini temizler. Belge manuel olarak güncellendikten veya yerleşim yeniden oluşturulduktan sonra bu yöntemi çağırın. |
| [get_Document](./get_document/)() const | Bu toplama örneğinin bağlı olduğu belgeyi alır veya ayarlar. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Düğümün bittiği sayfanın 1 tabanlı indeksini alır. Düğüm bir sayfaya eşlenemiyorsa 0 döndürür. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen düğüme karşılık gelen [LayoutEnumerator](../layoutenumerator/) nesnesinin opak bir konumunu döndürür. Döndürülen değeri, sayısı yapılan belge ile düğümün belgesi aynı olduğunda [Current](../layoutenumerator/get_current/) yöntemine argüman olarak kullanabilirsiniz. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen düğümün kapsadığı sayfa sayısını alır. Düğüm tek bir sayfadaysa 0 döndürür. Bu, [GetEndPageIndex()](../) - [GetStartPageIndex()](../) farkına eşittir. |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Düğümün başladığı sayfanın 1 tabanlı indeksini alır. Düğüm bir sayfaya eşlenemiyorsa 0 döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Bu sınıfın bir örneğini başlatır. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir [LayoutCollector](./) oluşturup bir [Document](../../aspose.words/document/) nesnesi belirttiğinizde, toplama, belge sayfalara biçimlendirildiğinde belge düğümlerinin yerleşim nesnelerine eşlemesini kaydeder.

Belirli bir belge düğümünün (ör. koşu, paragraf veya tablo hücresi) hangi sayfada bulunduğunu [GetStartPageIndex()](../), [GetEndPageIndex()](../) ve [GetNumPagesSpanned()](../) yöntemlerini kullanarak öğrenebilirsiniz. Bu yöntemler belge sayfa yerleşim modelini otomatik olarak oluşturur ve gerekirse alanları günceller.

Artık yerleşim bilgisi toplamanıza gerek kalmadığında, daha fazla yerleşim eşlemesinin gereksiz toplanmasını önlemek için [Document](./get_document/) özelliğini **null** olarak ayarlamak en iyisidir.

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
