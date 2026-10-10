---
title: "Aspose::Words::NodeCollection::Contains-Methode"
linktitle: "Contains"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeCollection::Contains-Methode. Bestimmt, ob ein Knoten in der Sammlung in C++ enthalten ist."
type: docs
weight: 4000
url: /de/cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


Bestimmt, ob ein Knoten in der Sammlung ist.

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Knoten | const System::SharedPtr\<Aspose::Words::Node\>\& | Der zu findende Knoten. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## Hinweise


Diese Methode führt eine lineare Suche durch; daher ist die durchschnittliche Ausführungszeit proportional zu [Count](../get_count/).

## Beispiele



Zeigt, wie man mit einer [NodeCollection](../) arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie dem Dokument Text hinzu, indem Sie Runs mit einem DocumentBuilder einfügen.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Jeder Aufruf der "Write"-Methode erzeugt ein neues Run,
// das dann in der RunCollection des übergeordneten Paragraphen erscheint.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// Wir können auch manuell einen Knoten in die RunCollection einfügen.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Greifen Sie auf einzelne Runs zu und entfernen Sie sie, um deren Text aus dem Dokument zu entfernen.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## Siehe auch

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
