---
title: "Aspose::Words::NodeCollection::Add-Methode"
linktitle: "Add"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeCollection::Add-Methode. Fügt einen Knoten am Ende der Sammlung in C++ hinzu."
type: docs
weight: 2000
url: /de/cpp/aspose.words/nodecollection/add/
---
## NodeCollection::Add method


Fügt einen Knoten am Ende der Sammlung hinzu.

```cpp
void Aspose::Words::NodeCollection::Add(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Knoten | const System::SharedPtr\<Aspose::Words::Node\>\& | Der Knoten, der am Ende der Sammlung hinzugefügt werden soll. |
## Hinweise


Der Knoten wird als Kind in das Knotenobjekt eingefügt, aus dem die Sammlung erstellt wurde.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie [ImportNode()](../) verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

## Beispiele



Zeigt, wie man einen neuen Abschnittsknoten zur Bearbeitung vorbereitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält einen Abschnitt, der einen Body hat, der wiederum einen Paragraphen enthält.
// Wir können diesem Dokument Inhalte hinzufügen, indem wir Elemente wie Textläufe, Formen oder Tabellen zu diesem Paragraphen hinzufügen.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Wenn wir einen neuen Abschnitt auf diese Weise hinzufügen, hat er keinen Body oder andere Kindknoten.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Führen Sie die Methode "EnsureMinimum" aus, um diesem Abschnitt einen Body und einen Paragraphen hinzuzufügen, damit Sie mit der Bearbeitung beginnen können.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Siehe auch

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
