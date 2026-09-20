---
title: "Перечисление Aspose::Words::Math::OfficeMathDisplayType"
linktitle: "OfficeMathDisplayType"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Math::OfficeMathDisplayType. Указывает тип формата отображения уравнения в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


Указывает тип формата отображения уравнения.

```cpp
enum class OfficeMathDisplayType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Display | 0 | Office [Math](../) отображается на отдельной строке. |
| Inline | 1 | Office [Math](../) отображается inline вместе с текстом. |


## Примеры



Показывает, как задать формат отображения офисной математики.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Узлы OfficeMath, являющиеся дочерними для других узлов OfficeMath, всегда inline.
// Узел, с которым мы работаем, является базовым узлом для изменения его расположения и типа отображения.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Измените расположение и тип отображения узла OfficeMath.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## См. также

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
