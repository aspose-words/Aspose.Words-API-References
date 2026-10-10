---
title: "Aspose::Words::Drawing::OleFormat::get_Clsid 方法"
linktitle: "get_Clsid"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OleFormat::get_Clsid 方法。获取 C++ 中 OLE 对象的 CLSID。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing/oleformat/get_clsid/
---
## OleFormat::get_Clsid method


获取 OLE 对象的 CLSID。

```cpp
System::Guid Aspose::Words::Drawing::OleFormat::get_Clsid()
```


## 示例



展示如何访问文档中嵌入的 OLE 控件及其子控件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE ActiveX controls.docm");

// Shapes 在文档主体中存储和显示 OLE 对象。
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(u"6e182020-f460-11ce-9bcd-00aa00608e01", System::ObjectExt::ToString(shape->get_OleFormat()->get_Clsid()));

auto oleControl = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(shape->get_OleFormat()->get_OleControl());

// 某些 OLE 控件可能包含子控件，例如本文件中具有三个选项按钮的控件。
System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControlCollection> oleControlCollection = oleControl->get_ChildNodes();

ASSERT_EQ(3, oleControlCollection->get_Count());

ASSERT_EQ(u"C#", oleControlCollection->idx_get(0)->get_Caption());
ASSERT_EQ(u"1", oleControlCollection->idx_get(0)->get_Value());

ASSERT_EQ(u"Visual Basic", oleControlCollection->idx_get(1)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(1)->get_Value());

ASSERT_EQ(u"Delphi", oleControlCollection->idx_get(2)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(2)->get_Value());
```

## 另见

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
