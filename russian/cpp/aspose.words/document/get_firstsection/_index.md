---
title: "Метод Aspose::Words::Document::get_FirstSection"
linktitle: "get_FirstSection"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_FirstSection. Получает первую секцию в документе на C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words/document/get_firstsection/
---
## Document::get_FirstSection method


Получает первый раздел в документе.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_FirstSection()
```


## Примеры



Показывает, как заменить текст в нижнем колонтитуле документа.
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


Показывает, как создать новую секцию с помощью DocumentBuilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит одну секцию по умолчанию,
// которая содержит дочерние узлы, которые мы можем редактировать.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Используйте DocumentBuilder, чтобы добавить текст в первую секцию.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Создайте вторую секцию, вставив разрыв секции.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Каждая секция имеет свои собственные настройки разметки страницы.
// Мы можем разбить текст во второй секции на две колонки.
// Это не повлияет на текст в первой секции.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```


Показывает, как перебрать дочерние элементы составного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Секция является составным узлом и может содержать дочерние узлы,
// но только если эти дочерние узлы имеют тип \"Body\" или \"HeaderFooter\".
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

## См. также

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
