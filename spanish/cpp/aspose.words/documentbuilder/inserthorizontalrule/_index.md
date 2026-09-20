---
title: "Aspose::Words::DocumentBuilder::InsertHorizontalRule método"
linktitle: "InsertHorizontalRule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertHorizontalRule método. Inserta una forma de regla horizontal en el documento en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder::InsertHorizontalRule method


Inserta una forma de regla horizontal en el documento.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertHorizontalRule()
```


### ReturnValue

La forma que es una regla horizontal.

## Ejemplos



Muestra cómo insertar una forma de regla horizontal y personalizar su formato.
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

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
