---
title: "Aspose::Words::Math::OfficeMath::get_Justification metod"
linktitle: "get_Justification"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Math::OfficeMath::get_Justification metod. Hämtar/sätter Office Math-justering i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.math/officemath/get_justification/
---
## OfficeMath::get_Justification method


Hämtar/sätter Office [Math](../../) justering.

```cpp
Aspose::Words::Math::OfficeMathJustification Aspose::Words::Math::OfficeMath::get_Justification()
```

## Anmärkningar


Justering kan inte sättas på Office [Math](../../) med displayformattypen [Inline](../../officemathdisplaytype/).

[Inline](../../../aspose.words/inline/) justification cannot be set to the Office [Math](../../) with display format type [Display](../../officemathdisplaytype/).

Motsvarande [DisplayType](../get_displaytype/) måste anges innan Office [Math](../../) justering sätts.

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

* Enum [OfficeMathJustification](../../officemathjustification/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
