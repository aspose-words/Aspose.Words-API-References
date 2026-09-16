---
title: "Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision 方法"
linktitle: "get_IsMoveToRevision"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision 方法。若在启用了更改跟踪的 Microsoft Word 中此对象被移动（插入），则返回 true。"
type: docs
weight: 34000
url: /zh/cpp/aspose.words.drawing/shapebase/get_ismovetorevision/
---
## ShapeBase::get_IsMoveToRevision method


如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision()
```


## 示例



展示如何识别移动修订形状。
```cpp
// 移动修订是指我们在 Microsoft Word 中通过剪切粘贴移动文档主体中的元素时，
// 跟踪更改。如果在此类文本移动中涉及内联形状，该形状也会成为修订。
// 复制粘贴或移动浮动形状不会产生移动修订。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// 移动修订由“Move from”和“Move to”修订对组成。我们在此文档中移动了一个形状，
// 但在接受或拒绝该移动修订之前，该形状会出现两个实例。
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// 这是“Move to”修订，即位于其到达目的地的形状。
// 如果我们接受该修订，这个“Move to”修订形状将消失，
// 而“Move from”修订形状将保留。
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// 这是“Move from”修订，即位于其原始位置的形状。
// 如果我们接受该修订，这个“Move from”修订形状将消失，
// 而“Move to”修订形状将保留。
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
