---
title: "Aspose::Words::Border::get_IsVisible 方法"
linktitle: "get_IsVisible"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Border::get_IsVisible 方法。如果 LineStyle 不是 None，则在 C++ 中返回 **true**。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/border/get_isvisible/
---
## Border::get_IsVisible method


如果 [LineStyle](../get_linestyle/) 不是 [None](../../linestyle/)，则返回 **true**。

```cpp
bool Aspose::Words::Border::get_IsVisible()
```


## 示例



展示如何从段落中移除边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// 每个段落都有各自的一组边框。
// 我们可以通过段落格式对象访问这些边框外观的设置。
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// 我们可以通过运行 ClearFormatting 方法一次性移除边框。
// 对段落的每个边框运行此方法将移除其所有边框。
for (auto&& border : System::IterateOver(borders))
{
    border->ClearFormatting();
}

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, borders->idx_get(0)->get_LineStyle());
ASSERT_FALSE(borders->idx_get(0)->get_IsVisible());

doc->Save(get_ArtifactsDir() + u"Border.ClearFormatting.docx");
```

## 另见

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
