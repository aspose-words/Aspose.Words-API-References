---
title: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked 方法"
linktitle: "get_AnchorLocked"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked 方法。指定形状''的锚点在 C++ 中是否被锁定。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


指定形状锚点是否被锁定。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## 备注


默认值为 **false**。

仅对顶层形状有效。

此属性影响形状在 Microsoft Word 中锚点的行为。当锚点未锁定时，在 Microsoft Word 中移动形状也会移动其锚点。

## 示例



展示如何锁定或解锁形状的段落锚点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// 将 \"AnchorLocked\" 属性设置为 \"true\" 以防止形状的锚点
// 在 Microsoft Word 中移动形状时不被移动。
// 将 \"AnchorLocked\" 属性设置为 \"false\" 以允许形状的任何移动
// 并使其锚点也移动到形状靠近的任何其他段落。
shape->set_AnchorLocked(anchorLocked);

// 如果形状左侧没有可见的锚点符号，
// 我们需要通过 \"Options\" -> \"Display\" -> \"Object Anchors\" 来启用可见锚点。
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
