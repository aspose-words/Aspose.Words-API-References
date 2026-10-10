---
title: "Aspose::Words::NodeCollection::Insert‑metod"
linktitle: "Infoga"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeCollection::Insert‑metod. Infogar en nod i samlingen på det angivna indexet i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/nodecollection/insert/
---
## NodeCollection::Insert method


Infogar en nod i samlingen på det angivna indexet.

```cpp
void Aspose::Words::NodeCollection::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Det nollbaserade indexet för noden. Negativa index är tillåtna och indikerar åtkomst från listans slut. Till exempel betyder -1 den sista noden, -2 den näst sista och så vidare. |
| nod | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden att infoga. |
## Anmärkningar


Noden infogas som ett barn i nodobjektet som samlingen skapades från.

Om indexet är lika med eller större än [Count](../get_count/), läggs noden till i slutet av samlingen.

Om indexet är negativt och dess absoluta värde är större än [Count](../get_count/), läggs noden till i slutet av samlingen.

Om noden som infogas skapades från ett annat dokument bör du använda [ImportNode()](../) för att importera noden till det aktuella dokumentet. Den importerade noden kan sedan infogas i det aktuella dokumentet.

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
