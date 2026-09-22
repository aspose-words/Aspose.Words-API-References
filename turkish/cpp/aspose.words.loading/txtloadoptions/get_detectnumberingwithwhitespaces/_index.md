---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces yöntemi"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces yöntemi. Belgenin düz metin formatından içe aktarılması sırasında numaralı liste öğelerinin nasıl tanındığını belirtmeye olanak tanır. Varsayılan değer C++'ta true'dur."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


Belge düz metin formatından içe aktarıldığında numaralı liste öğelerinin nasıl tanındığını belirtmeye olanak tanır. Varsayılan değer **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## Açıklamalar


Bu seçenek **false** olarak ayarlanırsa, liste tanıma algoritması, liste numaraları nokta, sağ parantez veya madde işareti (örneğin "•", "*", "-" veya "o") ile bittiğinde liste paragraflarını algılar.

Bu seçenek **true** olarak ayarlanırsa, boşluk karakterleri de liste numarası ayırıcıları olarak kullanılır: Arapça stil numaralandırma (1., 1.1.2.) için liste tanıma algoritması hem boşlukları hem de nokta (".") sembollerini kullanır.

## Örnekler



Düz metin belgeleri yüklenirken listelerin nasıl algılanacağını gösterir.
```cpp
// Dört ayrı parçaya sahip bir düz metin belgesini bir dize içinde oluşturun, bu parçaları listeler olarak yorumlayabiliriz,
// farklı ayırıcılarla. Düz metin belgesi bir "Document" nesnesine yüklendiğinde,
// Aspose.Words her zaman ilk üç listeyi algılar ve bir "List" nesnesi ekler
// her biri için belgenin "Lists" özelliğine.
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// "TxtLoadOptions" nesnesi oluşturun, bunu bir belgenin yapıcısına geçirebiliriz
// düz metin belgesini nasıl yüklediğimizi değiştirmek için.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// "DetectNumberingWithWhitespaces" özelliğini "true" olarak ayarlayın, numaralı öğeleri algılamak için
// boşluk ayırıcılarıyla, örneğin belgemizdeki dördüncü liste gibi, listeler olarak.
// Bu, sayılarla başlayan paragrafları da yanlışlıkla listeler olarak algılayabilir.
// "DetectNumberingWithWhitespaces" özelliğini "false" olarak ayarlayın
// boşluk ayırıcılarıyla numaralı öğelerden liste oluşturmamak için.
loadOptions->set_DetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    ASSERT_EQ(4, doc->get_Lists()->get_Count());
    ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
else
{
    ASSERT_EQ(3, doc->get_Lists()->get_Count());
    ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
```

## Ayrıca Bakınız

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
