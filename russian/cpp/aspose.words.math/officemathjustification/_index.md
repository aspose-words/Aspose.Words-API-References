---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Math::OfficeMathJustification enum. Указывает выравнивание уравнения в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


Указывает выравнивание уравнения.

```cpp
enum class OfficeMathJustification
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| CenterGroup | 1 | Выравнивает экземпляры математического текста по левому краю относительно друг друга и центрирует группу математического текста (the [Math](../)[Paragraph](../../aspose.words/paragraph/)) относительно страницы. |
| По центру | 2 | Центрирует каждый экземпляр математического текста индивидуально относительно полей. |
| Left | 3 | Выравнивание по левому краю [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Right | 4 | Выравнивание по правому краю [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Inline | 7 | Позиция [Inline](../../aspose.words/inline/) для [Math](../). |
| Default | n/a | Значение по умолчанию [CenterGroup](./). |


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
