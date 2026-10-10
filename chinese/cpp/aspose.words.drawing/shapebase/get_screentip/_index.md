---
title: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip 方法"
linktitle: "get_ScreenTip"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip 方法。定义当鼠标指针移动到形状上方时显示的文本（C++）。"
type: docs
weight: 46000
url: /zh/cpp/aspose.words.drawing/shapebase/get_screentip/
---
## ShapeBase::get_ScreenTip method


定义鼠标指针悬停在形状上时显示的文本。

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_ScreenTip()
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
