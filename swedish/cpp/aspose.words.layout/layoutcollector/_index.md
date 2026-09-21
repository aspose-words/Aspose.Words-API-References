---
title: "Aspose::Words::Layout::LayoutCollector klass"
linktitle: "LayoutCollector"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutCollector klass. Denna klass möjliggör att beräkna sidnummer för dokumentnoder. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


Denna klass möjliggör beräkning av sidnummer för dokumentnoder. För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutCollector : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clear](./clear/)() | Rensar all insamlad layoutdata. Anropa den här metoden efter att dokumentet har uppdaterats manuellt, eller efter att layouten har byggts om. |
| [get_Document](./get_document/)() const | Hämtar eller anger dokumentet som denna samlare är kopplad till. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar 1‑baserat index för sidan där noden slutar. Returnerar 0 om noden inte kan mappas till en sida. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar en opak position för [LayoutEnumerator](../layoutenumerator/) som motsvarar den angivna noden. Du kan använda det returnerade värdet som ett argument till [Current](../layoutenumerator/get_current/) förutsatt att det dokument som enumereras och dokumentet för noden är samma. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar antalet sidor som den angivna noden sträcker sig över. 0 om noden är inom en enda sida. Detta är samma som [GetEndPageIndex()](../) - [GetStartPageIndex()](../). |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar 1‑baserat index för sidan där noden börjar. Returnerar 0 om noden inte kan mappas till en sida. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initierar en instans av denna klass. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Sättare för [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/). |
| static [Type](./type/)() |  |
## Anmärkningar


När du skapar en [LayoutCollector](./) och anger ett [Document](../../aspose.words/document/) dokumentobjekt att fästa på, kommer samlaren att registrera mappning av dokumentnoder till layoutobjekt när dokumentet formateras till sidor.

Du kommer att kunna ta reda på på vilken sida en viss dokumentnod (t.ex. körning, stycke eller tabellcell) finns genom att använda metoderna [GetStartPageIndex()](../), [GetEndPageIndex()](../) och [GetNumPagesSpanned()](../). Dessa metoder bygger automatiskt sidlayoutmodellen för dokumentet och uppdaterar fält om det behövs.

När du inte längre behöver samla in layoutinformation är det bäst att sätta egenskapen [Document](./get_document/) till **null** för att undvika onödig insamling av fler layoutmappningar.

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
