---
title: "Aspose::Words::DocumentBuilder::InsertForms2OleControl metodu"
linktitle: "InsertForms2OleControl"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertForms2OleControl metodu. C++'ta mevcut konuma Forms2OleControl nesnesi ekler."
type: docs
weight: 35250
url: /tr/cpp/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder::InsertForms2OleControl method


Geçerli konuma [Forms2OleControl](../) nesnesi ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertForms2OleControl(const System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControl> &forms2OleControl)
```


### ReturnValue

[Shape](../../../aspose.words.drawing/shape/) object that contains passed [Forms2OleControl](../)

## Örnekler



ActiveX denetiminin nasıl ekleneceğini gösterir.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

auto button1 = System::MakeObject<Aspose::Words::Drawing::Ole::CommandButtonControl>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertForms2OleControl(button1);
ASSERT_EQ(Aspose::Words::Drawing::Ole::Forms2OleControlType::CommandButton, button1->get_Type());
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
