---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Math::OfficeMathJustification enum. Anger justeringen av ekvationen i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


Anger justeringen av ekvationen.

```cpp
enum class OfficeMathJustification
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| CenterGroup | 1 | Justerar instanser av matematisk text till vänster i förhållande till varandra, och centrerar gruppen av matematisk text (de [Math](../)[Paragraph](../../aspose.words/paragraph/)) i förhållande till sidan. |
| Centrerad | 2 | Centrerar varje instans av matematisk text individuellt i förhållande till marginalerna. |
| Left | 3 | Vänsterjustering av [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Right | 4 | Högerjustering av [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Inline | 7 | [Inline](../../aspose.words/inline/) position av [Math](../). |
| Default | n/a | Standardvärde [CenterGroup](./). |


## Exempel



Visar hur man ställer in visningsformatering för office math.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// OfficeMath-noder som är barn till andra OfficeMath-noder är alltid inline.
// Noden vi arbetar med är basnoden för att ändra dess plats och visningstyp.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Ändra platsen och visningstypen för OfficeMath-noden.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## Se även

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
