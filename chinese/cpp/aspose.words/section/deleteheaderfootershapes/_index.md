---
title: "Aspose::Words::Section::DeleteHeaderFooterShapes 方法"
linktitle: "DeleteHeaderFooterShapes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Section::DeleteHeaderFooterShapes 方法。删除此节在 C++ 中页眉和页脚中的所有形状（绘图对象）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/section/deleteheaderfootershapes/
---
## Section::DeleteHeaderFooterShapes method


删除该节页眉和页脚中的所有形状（绘图对象）。

```cpp
void Aspose::Words::Section::DeleteHeaderFooterShapes()
```


## 示例



展示如何从节的所有页眉和页脚中移除所有形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个带有形状的主页眉。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);

// 创建一个带有图像的主页脚。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->InsertImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// 从第一节的页眉和页脚中移除所有形状。
doc->get_FirstSection()->DeleteHeaderFooterShapes();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## 另见

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
