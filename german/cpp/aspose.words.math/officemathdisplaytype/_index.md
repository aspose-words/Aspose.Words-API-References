---
title: "Aspose::Words::Math::OfficeMathDisplayType enum"
linktitle: "OfficeMathDisplayType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Math::OfficeMathDisplayType‑Enum. Gibt den Anzeigetyp des Formats der Gleichung in C++ an."
type: docs
weight: 3000
url: /de/cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


Gibt den Anzeigeformattyp der Gleichung an.

```cpp
enum class OfficeMathDisplayType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Display | 0 | Das Office‑[Math](../) wird in einer eigenen Zeile angezeigt. |
| Inline | 1 | Das Office‑[Math](../) wird inline mit dem Text angezeigt. |


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

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
