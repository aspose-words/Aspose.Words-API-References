---
title: "Aspose::Words::Section::EnsureMinimum metod"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Section::EnsureMinimum metod. Säkerställer att avsnittet har Body med ett Paragraph i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/section/ensureminimum/
---
## Section::EnsureMinimum method


Säkerställer att avsnittet har [Body](../get_body/) med ett [Paragraph](../../paragraph/).

```cpp
void Aspose::Words::Section::EnsureMinimum()
```


## Exempel



Visar hur man förbereder en ny section node för redigering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ett tomt dokument kommer med ett avsnitt, som har en body, som i sin tur har ett paragraph.
// Vi kan lägga till innehåll i detta dokument genom att lägga till element såsom textkörningar, shapes eller tabeller till det paragraph.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Om vi lägger till ett nytt avsnitt på detta sätt, kommer det inte att ha en body, eller några andra child nodes.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Kör "EnsureMinimum"-metoden för att lägga till en body och ett paragraph till detta avsnitt för att börja redigera det.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Se även

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
