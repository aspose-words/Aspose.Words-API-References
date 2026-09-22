---
title: "Aspose::Words::Section::get_HeadersFooters yöntemi"
linktitle: "get_HeadersFooters"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Section::get_HeadersFooters yöntemi. Bölümün başlık ve altbilgi düğümlerine C++'ta erişim sağlar."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/section/get_headersfooters/
---
## Section::get_HeadersFooters method


Bölümün üstbilgi ve altbilgi düğümlerine erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooterCollection> Aspose::Words::Section::get_HeadersFooters()
```


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

* Class [HeaderFooterCollection](../../headerfootercollection/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
