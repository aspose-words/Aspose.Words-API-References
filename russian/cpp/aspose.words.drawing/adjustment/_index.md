---
title: "Aspose::Words::Drawing::Adjustment class"
linktitle: "Adjustment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Adjustment class. Представляет значения корректировки, применяемые к указанной фигуре в C++."
type: docs
weight: 334
url: /ru/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


Представляет значения корректировок, применяемые к указанной фигуре.

```cpp
class Adjustment : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Name](./get_name/)() const | Получает имя корректировки. |
| [get_Value](./get_value/)() const | Получает или задаёт необработанное значение корректировки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как работать с необработанными значениями корректировок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rounded rectangle shape.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> adjustments = shape->get_Adjustments();
ASSERT_EQ(1, adjustments->get_Count());

System::SharedPtr<Aspose::Words::Drawing::Adjustment> adjustment = adjustments->idx_get(0);
ASSERT_EQ(u"adj", adjustment->get_Name());
ASSERT_EQ(16667, adjustment->get_Value());

adjustment->set_Value(30000);

doc->Save(get_ArtifactsDir() + u"Shape.Adjustments.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
