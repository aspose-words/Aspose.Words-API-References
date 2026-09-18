---
title: "Aspose::Words::Document::EnsureMinimum-Methode"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::EnsureMinimum-Methode. Wenn das Dokument keine Abschnitte enthält, wird in C++ ein Abschnitt mit einem Absatz erstellt."
type: docs
weight: 10000
url: /de/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


Wenn das Dokument keine Abschnitte enthält, wird ein Abschnitt mit einem Absatz erstellt.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## Beispiele



Zeigt, wie man sicherstellt, dass ein Dokument die minimale Menge an Knoten enthält, die zum Bearbeiten seines Inhalts erforderlich sind.
```cpp
// Ein neu erstelltes Dokument enthält einen untergeordneten Abschnitt, der einen untergeordneten Body und einen untergeordneten Absatz umfasst.
// Wir können den Inhalt des Dokument‑Body bearbeiten, indem wir Knoten wie Runs oder Inline‑Shapes zu diesem Absatz hinzufügen.
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// Dies ist die minimale Menge an Knoten, die wir benötigen, um das Dokument bearbeiten zu können.
// Wir können das Dokument nicht mehr bearbeiten, wenn wir einen davon entfernen.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Rufen Sie diese Methode auf, um sicherzustellen, dass das Dokument mindestens diese drei Knoten enthält, damit wir es wieder bearbeiten können.
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
