---
title: "Aspose::Words::Math::OfficeMathDisplayType enum"
linktitle: "OfficeMathDisplayType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Math::OfficeMathDisplayType enum. Anger visningsformattypen för ekvationen i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


Anger visningsformattypen för ekvationen.

```cpp
enum class OfficeMathDisplayType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Display | 0 | Office [Math](../) visas på en egen rad. |
| Inline | 1 | Office [Math](../) visas inline med texten. |


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
