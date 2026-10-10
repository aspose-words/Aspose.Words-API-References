---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Math::OfficeMathJustification‑Enum. Gibt die Ausrichtung der Gleichung in C++ an."
type: docs
weight: 4000
url: /de/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


Gibt die Ausrichtung der Gleichung an.

```cpp
enum class OfficeMathJustification
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| CenterGroup | 1 | Richtet Instanzen mathematischen Textes zueinander linksbündig aus und zentriert die Gruppe des mathematischen Textes (das [Math](../)[Paragraph](../../aspose.words/paragraph/)) bezüglich der Seite. |
| Mitte | 2 | Zentriert jede Instanz mathematischen Textes einzeln in Bezug auf die Ränder. |
| Left | 3 | Linksbündige Ausrichtung des [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Right | 4 | Rechtsbündige Ausrichtung des [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Inline | 7 | [Inline](../../aspose.words/inline/) Position von [Math](../). |
| Default | n/a | Standardwert [CenterGroup](./). |


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
