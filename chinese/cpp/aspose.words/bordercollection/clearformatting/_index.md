---
title: "Aspose::Words::BorderCollection::ClearFormatting 方法"
linktitle: "ClearFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection::ClearFormatting 方法。移除 C++ 中对象的所有边框。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


移除对象的所有边框。

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## 示例



展示如何从文档中的所有段落移除所有边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// 本文档的第一段具有可见边框，使用以下设置。
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// 对每个段落使用 "ClearFormatting" 方法来移除所有边框。
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    paragraph->get_ParagraphFormat()->get_Borders()->ClearFormatting();

    for (auto&& border : System::IterateOver(paragraph->get_ParagraphFormat()->get_Borders()))
    {
        ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
        ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());
        ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
    }
}

doc->Save(get_ArtifactsDir() + u"BorderCollection.RemoveAllBorders.docx");
```

## 另见

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
