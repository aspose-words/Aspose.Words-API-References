---
title: "Aspose::Words::Drawing::ShapeBase::get_Target 方法"
linktitle: "get_Target"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_Target 方法。获取或设置形状超链接的目标框架（C++）。"
type: docs
weight: 50000
url: /zh/cpp/aspose.words.drawing/shapebase/get_target/
---
## ShapeBase::get_Target method


获取或设置形状超链接的目标框架。

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Target()
```

## 备注


默认值为空字符串。

## 示例



展示如何插入包含图像且也是超链接的形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// 在 Microsoft Word 中按 Ctrl 并左键单击形状将打开一个新的网页浏览器窗口
// 并将我们带到 "HRef" 属性中的超链接。
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
