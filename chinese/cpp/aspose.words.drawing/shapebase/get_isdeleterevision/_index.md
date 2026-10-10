---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision 方法"
linktitle: "get_IsDeleteRevision"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision 方法。返回 true，如果此对象在 Microsoft Word 中启用了更改跟踪时被删除（使用 C++）。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words.drawing/shapebase/get_isdeleterevision/
---
## ShapeBase::get_IsDeleteRevision method


如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision()
```


## 示例



展示如何使用修订形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// 插入一个不跟踪修订的内联形状，这将使该形状不属于任何修订。
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// 开始跟踪修订，然后插入另一个形状，该形状将成为修订。
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// 由于我们在跟踪更改时删除了该形状，
// 该形状仍保留在文档中，并计为删除修订。
// 接受此修订将永久删除该形状，拒绝则会保留在文档中。
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// 我们在跟踪更改时插入了另一个形状，因此该形状将计为插入修订。
// 接受此修订将把该形状合并到文档中，成为非修订的部分，
// 而拒绝此修订将永久删除该形状。
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
