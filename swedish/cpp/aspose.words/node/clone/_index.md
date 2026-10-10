---
title: "Aspose::Words::Node::Clone metod"
linktitle: "Klona"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Node::Clone metod. Skapar en dubblett av noden i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/node/clone/
---
## Node::Clone method


Skapar en kopia av noden.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| isCloneChildren | bool | Sant för att rekursivt klona delträdet under den angivna noden; falskt för att bara klona själva noden. |

### ReturnValue

Den klonade noden.
## Anmärkningar


Denna metod fungerar som en kopieringskonstruktor för noder. Den klonade noden har ingen förälder, men tillhör samma dokument som originalnoden.

Denna metod utför alltid en djup kopiering av noden. Parametern *isCloneChildren* anger om alla underordnade noder också ska kopieras.

## Exempel



Visar hur man klonar en sammansatt nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Nedan följer två sätt att klona en sammansatt nod.
// 1 -  Skapa en klon av en nod, och skapa också en klon av var och en av dess barnnoder.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Skapa en klon av en nod enbart själv utan några barn.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```

## Se även

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
