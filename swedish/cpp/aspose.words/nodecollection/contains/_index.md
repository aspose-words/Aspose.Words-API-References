---
title: "Aspose::Words::NodeCollection::Contains‑metod"
linktitle: "Contains"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeCollection::Contains‑metod. Avgör om en nod finns i samlingen i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


Avgör om en nod finns i samlingen.

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| nod | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden att hitta. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## Anmärkningar


Denna metod utför en linjär sökning; därför är den genomsnittliga exekveringstiden proportionell mot [Count](../get_count/).

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
