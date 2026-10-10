---
title: "Aspose::Words::Section::get_HeadersFooters Methode"
linktitle: "get_HeadersFooters"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::get_HeadersFooters Methode. Stellt in C++ Zugriff auf die Kopf- und Fußzeilenknoten des Abschnitts bereit."
type: docs
weight: 11000
url: /de/cpp/aspose.words/section/get_headersfooters/
---
## Section::get_HeadersFooters method


Bietet Zugriff auf die Knoten der Kopf- und Fußzeilen des Abschnitts.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooterCollection> Aspose::Words::Section::get_HeadersFooters()
```


## Beispiele



Zeigt, wie man alle Fußzeilen aus einem Dokument löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Iteriere durch jeden Abschnitt und entferne Fußzeilen aller Art.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Es gibt drei Arten von Fuß- und Kopfzeilentypen.
    // 1 -  Die \"Erste\" Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts erscheint.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  Die \"Primäre\" Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  Die \"Gerade\" Kopf-/Fußzeile, die auf geraden Seiten erscheint.
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

## Siehe auch

* Class [HeaderFooterCollection](../../headerfootercollection/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
