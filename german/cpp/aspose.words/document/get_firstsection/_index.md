---
title: "Aspose::Words::Document::get_FirstSection-Methode"
linktitle: "get_FirstSection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_FirstSection-Methode. Gibt den ersten Abschnitt im Dokument in C++ zurück."
type: docs
weight: 24000
url: /de/cpp/aspose.words/document/get_firstsection/
---
## Document::get_FirstSection method


Liest den ersten Abschnitt im Dokument.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_FirstSection()
```


## Beispiele



Zeigt, wie man Text in der Fußzeile eines Dokuments ersetzt.
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


Zeigt, wie man mit einem Document Builder einen neuen Abschnitt erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält standardmäßig einen Abschnitt,
// der Kindknoten enthält, die wir bearbeiten können.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Verwenden Sie einen Document Builder, um Text zum ersten Abschnitt hinzuzufügen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Erstellen Sie einen zweiten Abschnitt, indem Sie einen Abschnittsumbruch einfügen.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Jeder Abschnitt hat seine eigenen Seiteneinrichtungseinstellungen.
// Wir können den Text im zweiten Abschnitt in zwei Spalten aufteilen.
// Dies wirkt sich nicht auf den Text im ersten Abschnitt aus.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```


Zeigt, wie man durch die Kinder eines zusammengesetzten Knotens iteriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Ein Abschnitt ist ein zusammengesetzter Knoten und kann Kindknoten enthalten,
// aber nur, wenn diese Kindknoten vom Typ "Body" oder "HeaderFooter" sind.
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

## Siehe auch

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
