---
title: "Aspose::Words::Math::OfficeMath::get_DisplayType method"
linktitle: "get_DisplayType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Math::OfficeMath::get_DisplayType method. Ruft den Anzeigeformattyp von Office Math ab bzw. setzt ihn, der angibt, ob eine Gleichung inline mit dem Text oder in einer eigenen Zeile in C++ angezeigt wird."
type: docs
weight: 3000
url: /de/cpp/aspose.words.math/officemath/get_displaytype/
---
## OfficeMath::get_DisplayType method


Ruft den Anzeigeformattyp von Office [Math](../../) ab bzw. setzt ihn, der angibt, ob eine Gleichung inline mit dem Text oder in einer eigenen Zeile angezeigt wird.

```cpp
Aspose::Words::Math::OfficeMathDisplayType Aspose::Words::Math::OfficeMath::get_DisplayType()
```

## Hinweise


Der Anzeigeformattyp wirkt nur für Office [Math](../../) auf oberster Ebene.

Der zurückgegebene Anzeigeformattyp ist für verschachteltes Office [Math](../../) immer [Inline](../../officemathdisplaytype/).

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

* Enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
