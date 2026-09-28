---
title: "Aspose::Words::Drawing::AdjustmentCollection class"
linktitle: "AdjustmentCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::AdjustmentCollection class. Представляет собой только для чтения коллекцию значений Adjustment, применяемых к указанной фигуре в C++."
type: docs
weight: 667
url: /ru/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


Представляет собой только для чтения коллекцию значений [Adjustment](../adjustment/), применяемых к указанной фигуре.

```cpp
class AdjustmentCollection : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Count](./get_count/)() | Получает количество элементов, содержащихся в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает корректировку по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
