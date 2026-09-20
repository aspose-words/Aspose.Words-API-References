---
title: "Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat метод"
linktitle: "get_HorizontalRuleFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat метод. Предоставляет доступ к свойствам формы горизонтального правила. Для формы, которая не является горизонтальным правилом, возвращает null в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.drawing/shape/get_horizontalruleformat/
---
## Shape::get_HorizontalRuleFormat method


Предоставляет доступ к свойствам фигуры горизонтальной линии. Для фигуры, не являющейся горизонтальной линией, возвращает **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat()
```


## Примеры



Показывает, как вставить форму горизонтального правила и настроить её форматирование.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertHorizontalRule();

System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(Aspose::Words::Drawing::HorizontalRuleAlignment::Center);
horizontalRuleFormat->set_WidthPercent(70);
horizontalRuleFormat->set_Height(3);
horizontalRuleFormat->set_Color(System::Drawing::Color::get_Blue());
horizontalRuleFormat->set_NoShade(true);

ASSERT_TRUE(shape->get_IsHorizontalRule());
ASSERT_TRUE(shape->get_HorizontalRuleFormat()->get_NoShade());
```

## См. также

* Class [HorizontalRuleFormat](../../horizontalruleformat/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
