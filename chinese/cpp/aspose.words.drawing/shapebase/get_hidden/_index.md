---
title: "Aspose::Words::Drawing::ShapeBase::get_Hidden 方法"
linktitle: "get_Hidden"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_Hidden 方法。获取或设置一个布尔值，指示形状在 C++ 中是否可见。"
type: docs
weight: 22750
url: /zh/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


获取或设置一个布尔值，指示形状是否可见。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## 示例



展示如何隐藏形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
