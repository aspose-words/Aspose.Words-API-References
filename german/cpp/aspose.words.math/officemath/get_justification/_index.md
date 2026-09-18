---
title: "Aspose::Words::Math::OfficeMath::get_Justification-Methode"
linktitle: "get_Justification"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Math::OfficeMath::get_Justification-Methode. Liest/legt die Office Math‑Ausrichtung in C++ fest."
type: docs
weight: 5000
url: /de/cpp/aspose.words.math/officemath/get_justification/
---
## OfficeMath::get_Justification method


Liest/legt die Office [Math](../../)-Ausrichtung fest.

```cpp
Aspose::Words::Math::OfficeMathJustification Aspose::Words::Math::OfficeMath::get_Justification()
```

## Hinweise


Die Ausrichtung kann nicht für das Office [Math](../../) mit Anzeigeformattyp [Inline](../../officemathdisplaytype/) festgelegt werden.

[Inline](../../../aspose.words/inline/) justification cannot be set to the Office [Math](../../) with display format type [Display](../../officemathdisplaytype/).

Der entsprechende [DisplayType](../get_displaytype/) muss festgelegt werden, bevor die Ausrichtung des Office [Math](../../) gesetzt wird.

## Beispiele



Zeigt, wie man die Anzeigeformatierung von Office‑Math festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// OfficeMath‑Knoten, die Kinder anderer OfficeMath‑Knoten sind, sind immer inline.
// Der Knoten, mit dem wir arbeiten, ist der Basisknoten, um seine Position und Anzeigeart zu ändern.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Ändern Sie die Position und die Anzeigeart des OfficeMath‑Knotens.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## Siehe auch

* Enum [OfficeMathJustification](../../officemathjustification/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
