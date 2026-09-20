---
title: "Aspose::Words::Math::OfficeMath::get_DisplayType метод"
linktitle: "get_DisplayType"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Math::OfficeMath::get_DisplayType. Получает/устанавливает тип формата отображения Office Math, который определяет, отображается ли уравнение встроенно в текст или в отдельной строке в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.math/officemath/get_displaytype/
---
## OfficeMath::get_DisplayType method


Получает/устанавливает тип формата отображения Office [Math](../../), который определяет, отображается ли уравнение встроенно в текст или в отдельной строке.

```cpp
Aspose::Words::Math::OfficeMathDisplayType Aspose::Words::Math::OfficeMath::get_DisplayType()
```

## Примечания


Тип формата отображения влияет только на верхний уровень Office [Math](../../).

Возвращаемый тип формата отображения всегда [Inline](../../officemathdisplaytype/) для вложенного Office [Math](../../).

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

* Enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
