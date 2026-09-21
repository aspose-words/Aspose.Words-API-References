---
title: "Aspose::Words::TabStop::get_IsClear metod"
linktitle: "get_IsClear"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TabStop::get_IsClear metod. Returnerar true om detta tabbstopp rensar eventuella befintliga tabbstopp på denna position i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/tabstop/get_isclear/
---
## TabStop::get_IsClear method


Returnerar **true** om detta tabbstopp rensar eventuella befintliga tabbstopp på den här positionen.

```cpp
bool Aspose::Words::TabStop::get_IsClear()
```


## Exempel



Visar hur man arbetar med ett dokuments samling av tabbstopp.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 punkter är en "tum" på Microsoft Word:s tabbstopp-linjal.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Varje "tab"-tecken flyttar byggarens markör till platsen för nästa tabbstopp.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Varje stycke får sin tabbstopp-samling, som klonar sina värden från dokumentbyggarens tabbstopp-samling.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// En samling tabbstopp kan peka oss till TabStops före och efter vissa positioner.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Vi kan rensa ett styckes tabbstoppsamling för att återgå till standardtabb‑beteendet.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Se även

* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
