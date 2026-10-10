---
title: "Aspose::Words::DocumentBuilder::InsertForms2OleControl 方法"
linktitle: "InsertForms2OleControl"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertForms2OleControl 方法。将在 C++ 中将 Forms2OleControl 对象插入到当前位置。"
type: docs
weight: 35250
url: /zh/cpp/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder::InsertForms2OleControl method


在当前位置插入 [Forms2OleControl](../) 对象。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertForms2OleControl(const System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControl> &forms2OleControl)
```


### ReturnValue

[Shape](../../../aspose.words.drawing/shape/) object that contains passed [Forms2OleControl](../)

## 示例



展示如何插入 ActiveX 控件。
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

auto button1 = System::MakeObject<Aspose::Words::Drawing::Ole::CommandButtonControl>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertForms2OleControl(button1);
ASSERT_EQ(Aspose::Words::Drawing::Ole::Forms2OleControlType::CommandButton, button1->get_Type());
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
