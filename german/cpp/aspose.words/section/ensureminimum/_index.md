---
title: "Aspose::Words::Section::EnsureMinimum Methode"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::EnsureMinimum Methode. Stellt sicher, dass der Abschnitt ein Body mit einem Paragraphen in C++ hat."
type: docs
weight: 9000
url: /de/cpp/aspose.words/section/ensureminimum/
---
## Section::EnsureMinimum method


Stellt sicher, dass der Abschnitt ein [Body](../get_body/) mit einem [Paragraph](../../paragraph/) hat.

```cpp
void Aspose::Words::Section::EnsureMinimum()
```


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

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
