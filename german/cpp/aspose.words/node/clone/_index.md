---
title: "Aspose::Words::Node::Clone Methode"
linktitle: "Klonen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::Clone Methode. Erstellt ein Duplikat des Knotens in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/node/clone/
---
## Node::Clone method


Erstellt ein Duplikat des Knotens.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| isCloneChildren | bool | True, um den Teilbaum unter dem angegebenen Knoten rekursiv zu klonen; false, um nur den Knoten selbst zu klonen. |

### ReturnValue

Der geklonte Knoten.
## Hinweise


Diese Methode dient als Kopierkonstruktor für Knoten. Der geklonte Knoten hat keinen Elternknoten, gehört aber zum selben Dokument wie der Originalknoten.

Diese Methode führt immer eine tiefe Kopie des Knotens aus. Der *isCloneChildren*-Parameter gibt an, ob ebenfalls alle untergeordneten Knoten kopiert werden sollen.

## Beispiele



Zeigt, wie ein Composite-Knoten geklont wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Unten sind zwei Methoden zum Klonen eines Composite-Knotens aufgeführt.
// 1 -  Erstelle eine Kopie eines Knotens und erstelle ebenfalls eine Kopie jedes seiner Kindknoten.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Erstelle eine Kopie eines Knotens nur für sich selbst, ohne Kinder.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```

## Siehe auch

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
