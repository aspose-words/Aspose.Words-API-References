---
title: "Aspose::Words::Document::get_FirstSection metodu"
linktitle: "get_FirstSection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_FirstSection metodu. Belge içinde C++'da ilk bölümü alır."
type: docs
weight: 24000
url: /tr/cpp/aspose.words/document/get_firstsection/
---
## Document::get_FirstSection method


Belgedeki ilk bölümü alır.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_FirstSection()
```


## Örnekler



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


Bir belge oluşturucu ile yeni bir bölüm oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge varsayılan olarak bir bölüm içerir,
// ki içinde düzenleyebileceğimiz alt düğümler bulunur.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// İlk bölüme metin eklemek için bir belge oluşturucu kullanın.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Bir bölüm sonlandırması ekleyerek ikinci bir bölüm oluşturun.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Her bölümün kendi sayfa ayarları vardır.
// İkinci bölmedeki metni iki sütuna bölüştürebiliriz.
// Bu, ilk bölmedeki metni etkilemez.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```


Bir birleşik düğümün alt öğeleri üzerinde yineleme yapmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Bir Section, birleşik bir düğümdür ve alt düğümler içerebilir,
// ancak yalnızca bu alt düğümler "Body" veya "HeaderFooter" düğüm türünde ise.
for (auto&& node : System::IterateOver(section))
{
    switch (node->get_NodeType())
    {
        case Aspose::Words::NodeType::Body:
            {
                auto body = System::ExplicitCast<Aspose::Words::Body>(node);

                std::cout << "Body:" << std::endl;
                std::cout << System::String::Format(u"\t\"{0}\"", body->GetText().Trim()) << std::endl;
                break;
            }

        case Aspose::Words::NodeType::HeaderFooter:
            {
                auto headerFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(node);

                std::cout << System::String::Format(u"HeaderFooter type: {0}:", headerFooter->get_HeaderFooterType()) << std::endl;
                std::cout << System::String::Format(u"\t\"{0}\"", headerFooter->GetText().Trim()) << std::endl;
                break;
            }

        default:
            {
                throw System::Exception(u"Unexpected node type in a section.");
            }

    }
}
```

## Ayrıca Bakınız

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
