---
title: "Aspose::Words::NodeCollection::idx_get metod"
linktitle: "idx_get"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeCollection::idx_get metod. Hämtar en nod på det angivna indexet i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/nodecollection/idx_get/
---
## NodeCollection::idx_get method


Hämtar en nod vid det angivna indexet.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Ett index i nodsamlingen. |
## Anmärkningar


Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst sista och så vidare.

Om index är större än eller lika med antalet objekt i listan, returneras en null-referens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan, returneras en null-referens.

## Exempel



Visar hur man traverserar en sammansatt nods samling av barnnoder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Lägg till två run och en shape som barnnoder till det första stycket i detta dokument.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Observera att 'CustomNodeId' inte sparas till en utdatafil och endast existerar under nodens livstid.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Iterera genom styckets samling av omedelbara barn,
// och skriv ut eventuella run eller shapes som vi hittar där.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## Se även

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
