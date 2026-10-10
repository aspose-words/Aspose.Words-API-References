---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StoryType enum. Word 文档的文本存储在 story 中。StoryType 在 C++ 中标识一个 story。"
type: docs
weight: 117000
url: /zh/cpp/aspose.words/storytype/
---
## StoryType enum


Word 文档的文本存储在 stories 中。[StoryType](./) 标识一个 story。

```cpp
enum class StoryType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 默认值。文档中不存在此类 story。 |
| MainText | 1 | 包含文档的主体文本，由 [Body](../body/) 表示。 |
| Footnotes | 2 | 包含脚注文本，由 [Footnote](../../aspose.words.notes/footnote/) 表示。 |
| Endnotes | 3 | 包含尾注文本，由 [Footnote](../../aspose.words.notes/footnote/) 表示。 |
| Comments | 4 | 包含文档注释（标注），由 [Comment](../comment/) 表示。 |
| Textbox | 5 | 包含形状或文本框文本，由 [Shape](../../aspose.words.drawing/shape/) 表示。 |
| EvenPagesHeader | 6 | 包含偶数页页眉的文本，由 [HeaderFooter](../headerfooter/) 表示。 |
| PrimaryHeader | 7 | 包含主页眉的文本。当奇偶页的页眉不同，包含奇数页页眉的文本。由 [HeaderFooter](../headerfooter/) 表示。 |
| EvenPagesFooter | 8 | 包含偶数页页脚的文本，由 [HeaderFooter](../headerfooter/) 表示。 |
| PrimaryFooter | 9 | 包含主页脚的文本。当奇偶页的页脚不同，包含奇数页页脚的文本。由 [HeaderFooter](../headerfooter/) 表示。 |
| FirstPageHeader | 10 | 包含首页页眉的文本，由 [HeaderFooter](../headerfooter/) 表示。 |
| FirstPageFooter | 11 | 包含首页页脚的文本，由 [HeaderFooter](../headerfooter/) 表示。 |
| FootnoteSeparator | 12 | 包含脚注分隔符的文本。 |
| FootnoteContinuationSeparator | 13 | 包含脚注续页分隔符的文本。 |
| FootnoteContinuationNotice | 14 | 包含脚注续页通知分隔符的文本。 |
| EndnoteSeparator | 15 | 包含尾注分隔符的文本。 |
| EndnoteContinuationSeparator | 16 | 包含尾注续页分隔符的文本。 |
| EndnoteContinuationNotice | 17 | 包含尾注续页通知分隔符的文本。 |


## 示例



展示如何从节点中移除所有形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用 DocumentBuilder 插入形状。这是一个内联形状，
// 它有一个父 Paragraph，该 Paragraph 是第一节 Body 的子节点。
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// 我们可以删除此 Body 的子段落中的所有形状。
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
