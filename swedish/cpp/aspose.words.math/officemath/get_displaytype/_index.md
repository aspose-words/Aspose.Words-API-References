---
title: "Aspose::Words::Math::OfficeMath::get_DisplayType metod"
linktitle: "get_DisplayType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Math::OfficeMath::get_DisplayType metod. Hämtar/sätter Office Math visningsformattyp som representerar om en ekvation visas inline med texten eller på en egen rad i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.math/officemath/get_displaytype/
---
## OfficeMath::get_DisplayType method


Hämtar/sätter Office [Math](../../) visningsformattyp som representerar om en ekvation visas inline med texten eller på en egen rad.

```cpp
Aspose::Words::Math::OfficeMathDisplayType Aspose::Words::Math::OfficeMath::get_DisplayType()
```

## Anmärkningar


Visningsformattypen har endast effekt för Office [Math](../../) på topnivå.

Den returnerade visningsformattypen är alltid [Inline](../../officemathdisplaytype/) för nästlad Office [Math](../../).

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

* Enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
