---
title: "Aspose::Words::HeaderFooterCollection::LinkToPrevious metod"
linktitle: "LinkToPrevious"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::HeaderFooterCollection::LinkToPrevious metod. Länkar eller avlänkar den angivna sidhuvudet eller sidfoten till motsvarande sidhuvud eller sidfot i föregående avsnitt i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/headerfootercollection/linktoprevious/
---
## HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType, bool) method


Länkar eller avlänkar det angivna sidhuvudet eller sidfoten till motsvarande sidhuvud eller sidfot i föregående avsnitt.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType headerFooterType, bool isLinkToPrevious)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Ett [HeaderFooterType](../../headerfootertype/)‑värde som specificerar sidhuvudet eller sidfoten att länka/avlänka. |
| isLinkToPrevious | bool | **true** för att länka sidhuvudet eller sidfoten till föregående avsnitt; **false** för att avlänka. |
## Anmärkningar


Om sidhuvudet eller sidfoten av den angivna typen inte finns, skapas det automatiskt.

## Exempel



Visar hur man länkar sidhuvuden och sidfötter mellan avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Gå till det första avsnittet och skapa ett sidhuvud och en sidfot. Som standard,
// sidhuvudet och sidfoten kommer endast att visas på sidor i det avsnitt som innehåller dem.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Vi kan länka ett avsnitts sidhuvuden/sidfötter till föregående avsnitts sidhuvuden/sidfötter
// för att låta det länkade avsnittet visa det länkade avsnittets sidhuvuden/sidfötter.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Varje avsnitt kommer fortfarande att ha sina egna sidhuvud-/sidfot-objekt. När vi länkar avsnitt,
// länkningsavsnittet kommer att visa det länkade avsnittets sidhuvuden/sidfötter samtidigt som det behåller sina egna.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Länka sidhuvudena/sidfötterna i det tredje avsnittet till sidhuvudena/sidfötterna i det andra avsnittet.
// Det andra avsnittet länkar redan till det första avsnittets sidhuvuden/sidfötter,
// så att länka till det andra avsnittet kommer att skapa en länkkedja.
// Det första, andra och nu det tredje avsnittet kommer alla att visa det första avsnittets sidhuvuden.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Vi kan avlänka ett föregående avsnitts sidhuvuden/sidfötter genom att skicka "false" när vi anropar metoden LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Vi kan också välja endast en specifik typ av sidhuvud/sidfot att länka med hjälp av den här metoden.
// Det tredje avsnittet kommer nu att ha samma sidfot som det andra och första avsnittet, men inte sidhuvudet.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Det första avsnittets sidhuvuden/sidfötter kan inte länka sig själva till något eftersom det inte finns något föregående avsnitt.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Alla det andra avsnittets sidhuvuden/sidfötter är länkade till det första avsnittets sidhuvuden/sidfötter.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// I det tredje avsnittet är endast sidfoten länkad till det första avsnittets sidfot via det andra avsnittet.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Se även

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::LinkToPrevious(bool) method


Länkar eller avlänkar alla sidhuvuden och sidfötter till motsvarande sidhuvuden och sidfötter i föregående avsnitt.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(bool isLinkToPrevious)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| isLinkToPrevious | bool | **true** för att länka sidhuvuden och sidfötter till föregående avsnitt; **false** för att avlänka dem. |
## Anmärkningar


Om någon av sidhuvudena eller sidfötterna inte finns, skapas de automatiskt.

## Exempel



Visar hur man länkar sidhuvuden och sidfötter mellan avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Gå till det första avsnittet och skapa ett sidhuvud och en sidfot. Som standard,
// sidhuvudet och sidfoten kommer endast att visas på sidor i det avsnitt som innehåller dem.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Vi kan länka ett avsnitts sidhuvuden/sidfötter till föregående avsnitts sidhuvuden/sidfötter
// för att låta det länkade avsnittet visa det länkade avsnittets sidhuvuden/sidfötter.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Varje avsnitt kommer fortfarande att ha sina egna sidhuvud-/sidfot-objekt. När vi länkar avsnitt,
// länkningsavsnittet kommer att visa det länkade avsnittets sidhuvuden/sidfötter samtidigt som det behåller sina egna.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Länka sidhuvudena/sidfötterna i det tredje avsnittet till sidhuvudena/sidfötterna i det andra avsnittet.
// Det andra avsnittet länkar redan till det första avsnittets sidhuvuden/sidfötter,
// så att länka till det andra avsnittet kommer att skapa en länkkedja.
// Det första, andra och nu det tredje avsnittet kommer alla att visa det första avsnittets sidhuvuden.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Vi kan avlänka ett föregående avsnitts sidhuvuden/sidfötter genom att skicka "false" när vi anropar metoden LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Vi kan också välja endast en specifik typ av sidhuvud/sidfot att länka med hjälp av den här metoden.
// Det tredje avsnittet kommer nu att ha samma sidfot som det andra och första avsnittet, men inte sidhuvudet.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Det första avsnittets sidhuvuden/sidfötter kan inte länka sig själva till något eftersom det inte finns något föregående avsnitt.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Alla det andra avsnittets sidhuvuden/sidfötter är länkade till det första avsnittets sidhuvuden/sidfötter.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// I det tredje avsnittet är endast sidfoten länkad till det första avsnittets sidfot via det andra avsnittet.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Se även

* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
