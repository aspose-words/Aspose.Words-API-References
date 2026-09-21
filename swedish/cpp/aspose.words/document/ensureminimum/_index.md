---
title: "Aspose::Words::Document::EnsureMinimum‑metod"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::EnsureMinimum‑metod. Om dokumentet inte innehåller några sektioner skapas en sektion med ett stycke i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


Om dokumentet inte innehåller några sektioner, skapas en sektion med ett stycke.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## Exempel



Visar hur man säkerställer att ett dokument innehåller den minsta uppsättningen noder som krävs för att redigera dess innehåll.
```cpp
// Ett nyss skapat dokument innehåller en underordnad Section, som inkluderar en underordnad Body och ett underordnat Paragraph.
// Vi kan redigera dokumentets Body-innehåll genom att lägga till noder som Runs eller inbäddade Shapes till det stycket.
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// Detta är den minsta uppsättningen noder som vi behöver för att kunna redigera dokumentet.
// Vi kommer inte längre kunna redigera dokumentet om vi tar bort någon av dem.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Anropa den här metoden för att säkerställa att dokumentet har minst dessa tre noder så att vi kan redigera det igen.
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
