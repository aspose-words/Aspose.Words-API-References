---
title: "Aspose::Words::Layout::LayoutCollector::GetEntity metod"
linktitle: "GetEntity"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutCollector::GetEntity metod. Returnerar en opak position av LayoutEnumerator som motsvarar den angivna noden. Du kan använda det returnerade värdet som ett argument till Current förutsatt att det dokument som enumereras och dokumentet för noden är samma i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


Returnerar en opak position av [LayoutEnumerator](../../layoutenumerator/) som motsvarar den angivna noden. Du kan använda det returnerade värdet som ett argument till [Current](../../layoutenumerator/get_current/) förutsatt att det dokument som enumereras och dokumentet för noden är samma.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## Anmärkningar


Denna metod fungerar endast för [Paragraph](../../../aspose.words/paragraph/) noder, samt odelbara inline‑noder, t.ex. [BookmarkStart](../../../aspose.words/bookmarkstart/) eller [Shape](../../../aspose.words.drawing/shape/). Den fungerar inte för [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) eller [Table](../../../aspose.words.tables/table/) noder, samt noder i sidhuvud/sidfot.

Observera att enheten som returneras för en [Paragraph](../../../aspose.words/paragraph/) nod är ett styckebrytningselement. Använd lämplig metod för att gå upp till föräldralinjen.

Om du behöver navigera till ett [Run](../../../aspose.words/run/) av text kan du infoga ett bokmärke precis före det och sedan navigera till bokmärket istället.

Om du behöver navigera till en [Cell](../../../aspose.words.tables/cell/) nod kan du gå till en [Paragraph](../../../aspose.words/paragraph/) nod i den här cellen och sedan gå upp till en föräldraenhet. Samma tillvägagångssätt kan användas för [Row](../../../aspose.words.tables/row/) och [Table](../../../aspose.words.tables/table/) noder.

## Exempel



Visar hur man ser de sidintervall som en nod sträcker sig över.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// Anropa metoden "GetNumPagesSpanned" för att räkna hur många sidor innehållet i vårt dokument sträcker sig över.
// Eftersom dokumentet är tomt är det antalet sidor för närvarande noll.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Fyll i dokumentet med 5 sidor innehåll.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Innan layoutsamlaren måste vi anropa metoden "UpdatePageLayout" för att ge oss
// en exakt siffra för någon layoutrelaterad mätning, såsom sidantalet.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// Vi kan se siffrorna för start- och slutssidorna för vilken nod som helst och deras totala sidintervall.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// Vi kan iterera över layout‑entiteterna med en LayoutEnumerator.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// LayoutEnumerator kan traversera samlingen av layout‑entiteter som ett träd.
// Vi kan också tillämpa den på motsvarande layout‑entitet för vilken nod som helst.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## Se även

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
