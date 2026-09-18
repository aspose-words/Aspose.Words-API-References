---
title: "Aspose::Words::CompositeNode::get_Count-Methode"
linktitle: "get_Count"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::get_Count-Methode. Gibt die Anzahl der unmittelbaren Kindknoten dieses Knotens in C++ zurück."
type: docs
weight: 4000
url: /de/cpp/aspose.words/compositenode/get_count/
---
## CompositeNode::get_Count method


Ermittelt die Anzahl der direkten Kindknoten dieses Knotens.

```cpp
int32_t Aspose::Words::CompositeNode::get_Count()
```


## Beispiele



Zeigt, wie man Kindknoten in der Sammlung von Kindern eines [CompositeNode](../) hinzufügt, aktualisiert und löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält standardmäßig einen Absatz.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Composite‑Knoten wie unser Absatz können andere Composite‑ und Inline‑Knoten als Kinder enthalten.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Erstelle drei weitere Run‑Knoten.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Der Dokumentkörper zeigt diese Runs nicht an, bis wir sie in einen Composite‑Knoten einfügen
// der selbst Teil des Knotensystems des Dokuments ist, wie wir es beim ersten Run getan haben.
// Wir können bestimmen, wo der Textinhalt von Knoten, die wir einfügen,
// im Dokument erscheint, indem wir einen Einfügeort relativ zu einem anderen Knoten im Absatz angeben.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Füge den zweiten Run in den Absatz vor dem initialen Run ein.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Füge den dritten Run nach dem initialen Run ein.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Füge den ersten Run am Anfang der Kindknoten‑Sammlung des Absatzes ein.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Wir können den Inhalt des Runs ändern, indem wir vorhandene Kindknoten bearbeiten und löschen.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## Siehe auch

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
