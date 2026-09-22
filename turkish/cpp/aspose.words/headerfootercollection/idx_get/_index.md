---
title: "Aspose::Words::HeaderFooterCollection::idx_get metodu"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::HeaderFooterCollection::idx_get metodu. C++'da belirtilen türde bir HeaderFooter alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/headerfootercollection/idx_get/
---
## HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType) method


Belirtilen türde bir [HeaderFooter](../../headerfooter/) alır.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Alınacak başlık/alt bilgi türünü belirten bir [HeaderFooterType](../../headerfootertype/) değeri. |

## Örnekler



Bir belgeden tüm altbilgileri silmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Her bölümü dolaşın ve her türlü altbilgiyi kaldırın.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Üstbilgi ve altbilgi türlerinin üç çeşidi vardır.
    // 1 -  \"First\" üstbilgi/altbilgi, yalnızca bir bölümün ilk sayfasında görünür.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  \"Primary\" üstbilgi/altbilgi, tek sayfalarda görünür.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  \"Even\" üstbilgi/altbilgi, çift sayfalarda görünür.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```


Bir belgenin altbilgisindeki metni nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```

## Ayrıca Bakınız

* Class [HeaderFooter](../../headerfooter/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::idx_get(int32_t) method


Verilen indeksteki bir [HeaderFooter](../../headerfooter/) alır.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Koleksiyona bir indeks. |
## Açıklamalar


İndeks sıfır tabanlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

İndeks listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

İndeks negatif ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

## Örnekler



Bölümler arasında üstbilgi ve altbilgileri nasıl bağlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// İlk bölüme geçin ve bir üstbilgi ile bir altbilgi oluşturun. Varsayılan olarak,
// üstbilgi ve altbilgi yalnızca onları içeren bölümdeki sayfalarda görünecektir.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Bir bölümün üstbilgi/altbilgilerini önceki bölümün üstbilgi/altbilgilerine bağlayabiliriz
// bağlayan bölümün, bağlanan bölümün üstbilgi/altbilgilerini görüntülemesine izin vermek için.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Her bölüm hâlâ kendi üstbilgi/altbilgi nesnelerine sahip olacaktır. Bölümleri bağladığımızda,
// bağlayan bölüm, kendi üstbilgi/altbilgilerini korurken bağlanan bölümün üstbilgi/altbilgilerini gösterecektir.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Üçüncü bölümün üstbilgi/altbilgilerini ikinci bölümün üstbilgi/altbilgilerine bağlayın.
// İkinci bölüm zaten birinci bölümün üstbilgi/altbilgilerine bağlanmıştır,
// bu yüzden ikinci bölüme bağlamak bir bağ zinciri oluşturur.
// Birinci, ikinci ve artık üçüncü bölümler, birinci bölümün üstbilgilerini gösterecek.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// LinkToPrevious yöntemini çağırırken "false" geçirerek önceki bir bölümün üstbilgi/altbilgilerini bağlamayı kaldırabiliriz.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Bu yöntemi kullanarak yalnızca belirli bir üstbilgi/altbilgi türünü bağlamayı seçebiliriz.
// Üçüncü bölüm artık ikinci ve birinci bölümlerle aynı altbilgiye sahip olacak, ancak üstbilgiye sahip olmayacak.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Birinci bölümün üstbilgi/altbilgileri, önceki bir bölüm olmadığı için kendilerini hiçbir şeye bağlayamaz.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// İkinci bölümün tüm üstbilgi/altbilgileri birinci bölümün üstbilgi/altbilgilerine bağlanmıştır.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Üçüncü bölümde, yalnızca alt bilgi, ikinci bölüm aracılığıyla birinci bölümün alt bilgisine bağlanır.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Ayrıca Bakınız

* Class [HeaderFooter](../../headerfooter/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
