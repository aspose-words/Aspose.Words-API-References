---
title: "Aspose::Words::Node::get_ParentNode metod"
linktitle: "get_ParentNode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Node::get_ParentNode metod. Hämtar den omedelbara föräldern till detta nod i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


Hämtar den omedelbara föräldern till den här noden.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## Anmärkningar


Om en nod precis har skapats och ännu inte har lagts till i trädet, eller om den har tagits bort från trädet, är föräldern **null**.

## Exempel



Visar hur man får åtkomst till en nods föräldranod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Lägg till en underordnad Run-nod i dokumentets första stycke.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Stycket är föräldranoden till run-noden. Vi kan spåra detta släktträd
// hela vägen till dokumentnoden, som är roten i dokumentets nodträd.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


Visar hur man skapar en nod och anger dess ägardokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Vi har ännu inte lagt till detta stycke som ett barn till någon sammansatt nod.
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// Om en nod är en lämplig barnnodtyp för en annan sammansatt nod,
// kan vi fästa den som ett barn endast om båda noderna har samma ägardokument.
// Ägardokumentet är det dokument vi skickade till nodens konstruktor.
// Vi har inte bifogat detta stycke till dokumentet, så dokumentet innehåller inte dess text.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// Eftersom dokumentet äger detta stycke kan vi tillämpa en av dess stilar på styckets innehåll.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// Lägg till denna nod i dokumentet och verifiera sedan dess innehåll.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Se även

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
