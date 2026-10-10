---
title: "Aspose::Words::NodeCollection::Insert-Methode"
linktitle: "Insert"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeCollection::Insert-Methode. Fügt einen Knoten in die Sammlung an dem angegebenen Index in C++ ein."
type: docs
weight: 10000
url: /de/cpp/aspose.words/nodecollection/insert/
---
## NodeCollection::Insert method


Fügt einen Knoten in die Sammlung am angegebenen Index ein.

```cpp
void Aspose::Words::NodeCollection::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Der nullbasierte Index des Knotens. Negative Indizes sind erlaubt und bedeuten den Zugriff vom Ende der Liste aus. Zum Beispiel bedeutet -1 den letzten Knoten, -2 den vorletzten und so weiter. |
| Knoten | const System::SharedPtr\<Aspose::Words::Node\>\& | Der einzufügende Knoten. |
## Hinweise


Der Knoten wird als Kind in das Knotenobjekt eingefügt, aus dem die Sammlung erstellt wurde.

Wenn der Index gleich oder größer als [Count](../get_count/) ist, wird der Knoten am Ende der Sammlung hinzugefügt.

Wenn der Index negativ ist und sein absoluter Wert größer als [Count](../get_count/) ist, wird der Knoten am Ende der Sammlung hinzugefügt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie [ImportNode()](../) verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

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
