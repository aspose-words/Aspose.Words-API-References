---
title: "Aspose::Words::NodeCollection::Remove metod"
linktitle: "Ta bort"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeCollection::Remove metod. Tar bort noden från samlingen och från dokumentet i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/nodecollection/remove/
---
## NodeCollection::Remove method


Tar bort noden från samlingen och från dokumentet.

```cpp
void Aspose::Words::NodeCollection::Remove(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| nod | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden som ska tas bort. |

## Exempel



Visar hur man arbetar med en [NodeCollection](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till text i dokumentet genom att infoga Run‑element med en DocumentBuilder.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Varje anrop av "Write"‑metoden skapar en ny Run,
// som sedan visas i föräldra‑Paragraphs RunCollection.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// Vi kan också infoga en nod i RunCollection manuellt.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Åtkomst till enskilda run‑element och ta bort dem för att ta bort deras text från dokumentet.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## Se även

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
