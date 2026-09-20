---
title: "Aspose::Words::Drawing::HorizontalRuleAlignment перечисление"
linktitle: "HorizontalRuleAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::HorizontalRuleAlignment перечисление. Представляет выравнивание указанного горизонтального правила в C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enum


Представляет выравнивание для указанного горизонтального правила.

```cpp
enum class HorizontalRuleAlignment
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Слева | 0 | Выровнено по левому краю. |
| По центру | 1 | Выровнено по центру. |
| Справа | 2 | Выровнено по правому краю. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
