---
title: "Метод Aspose::Words::Math::OfficeMath::get_ParentParagraph"
linktitle: "get_ParentParagraph"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Math::OfficeMath::get_ParentParagraph. Получает родительский Paragraph этого узла в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.math/officemath/get_parentparagraph/
---
## OfficeMath::get_ParentParagraph method


Получает родительский [Paragraph](../../../aspose.words/paragraph/) этого узла.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Math::OfficeMath::get_ParentParagraph()
```


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

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
