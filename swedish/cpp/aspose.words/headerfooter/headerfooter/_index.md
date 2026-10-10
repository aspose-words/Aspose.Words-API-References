---
title: "Aspose::Words::HeaderFooter::HeaderFooter konstruktor"
linktitle: "HeaderFooter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::HeaderFooter::HeaderFooter konstruktor. Skapar ett nytt sidhuvud eller en sidfot av den angivna typen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter::HeaderFooter constructor


Skapar ett nytt sidhuvud eller sidfot av den angivna typen.

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
| headerFooterType | Aspose::Words::HeaderFooterType | Ett [HeaderFooterType](../get_headerfootertype/) värde som specificerar typen av sidhuvud eller sidfot. |
## Anmärkningar


När [HeaderFooter](../) skapas, tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och [ParentNode](../../node/get_parentnode/) är **null**.

För att lägga till [HeaderFooter](../) till en [Section](../../section/) använd [InsertAfter1()</see>, <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../), eller [HeadersFooters](../../section/get_headersfooters/) egenskapen och metoderna [Add()](../), [Insert()](../).

## Exempel



Visar hur man skapar ett sidhuvud och en sidfot.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa ett sidhuvud och lägg till ett stycke i det. Texten i det stycket
// kommer att visas högst upp på varje sida i detta avsnitt, ovanför huvudtexten.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Skapa en sidfot och lägg till ett stycke i den. Texten i det stycket
// kommer att visas längst ner på varje sida i detta avsnitt, under huvudtexten.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## Se även

* Class [DocumentBase](../../documentbase/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
