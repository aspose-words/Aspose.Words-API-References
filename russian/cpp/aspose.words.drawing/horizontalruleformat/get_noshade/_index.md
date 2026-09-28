---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade метод"
linktitle: "get_NoShade"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade. Указывает наличие 3D‑затенения для горизонтальной линии. Если true, то горизонтальная линия без 3D‑затенения и используется сплошной цвет в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


Указывает наличие 3D‑теней для горизонтальной линии. Если **true**, то горизонтальная линия без 3D‑теней и используется сплошной цвет.

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## Примечания


Значение по умолчанию — **false**.

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

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
