---
title: "Método Aspose::Words::DocumentBuilder::InsertForms2OleControl"
linktitle: "InsertForms2OleControl"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::InsertForms2OleControl. Inserta un objeto Forms2OleControl en la posición actual en C++."
type: docs
weight: 35250
url: /es/cpp/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder::InsertForms2OleControl method


Inserta el objeto [Forms2OleControl](../) en la posición actual.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertForms2OleControl(const System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControl> &forms2OleControl)
```


### ReturnValue

[Shape](../../../aspose.words.drawing/shape/) object that contains passed [Forms2OleControl](../)

## Ejemplos



Muestra cómo insertar un control ActiveX.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

auto button1 = System::MakeObject<Aspose::Words::Drawing::Ole::CommandButtonControl>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertForms2OleControl(button1);
ASSERT_EQ(Aspose::Words::Drawing::Ole::Forms2OleControlType::CommandButton, button1->get_Type());
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
