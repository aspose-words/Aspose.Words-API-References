---
title: "Aspose::Words::CompositeNode::GetChild-Methode"
linktitle: "GetChild"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::GetChild-Methode. Gibt den N‑ten Kindknoten zurück, der dem angegebenen Typ entspricht, in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/compositenode/getchild/
---
## CompositeNode::GetChild method


Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::GetChild(Aspose::Words::NodeType nodeType, int32_t index, bool isDeep)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Gibt den Typ des Kindknotens an. |
| index | int32_t | Nullbasierter Index des auszuwählenden Kindknotens. Negative Indizes sind ebenfalls zulässig und bedeuten den Zugriff vom Ende, d. h. -1 bedeutet der letzte Knoten. |
| isDeep | bool | **true** zum rekursiven Auswählen aller Kindknoten; **false** zum Auswählen nur unter unmittelbaren Kindknoten. Siehe Anmerkungen für weitere Informationen. |

### ReturnValue

Der Kindknoten, der den Kriterien entspricht, oder **null**, wenn kein passender Knoten gefunden wird.
## Hinweise


Wenn der Index außerhalb des Bereichs liegt, wird ein **null** zurückgegeben.

## Beispiele



Zeigt, wie man durch die Sammlung von Kindknoten eines Composite-Knotens traversiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Füge zwei Runs und eine Form als Kindknoten zum ersten Absatz dieses Dokuments hinzu.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Beachten Sie, dass die 'CustomNodeId' nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Iterieren Sie durch die Sammlung unmittelbarer Kinder des Absatzes,
// und geben Sie alle Runs oder Shapes aus, die wir darin finden.
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

## Siehe auch

* Class [Node](../../node/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
