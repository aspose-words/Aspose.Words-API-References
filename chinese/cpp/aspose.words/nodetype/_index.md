---
title: "Aspose::Words::NodeType 枚举"
linktitle: "NodeType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeType 枚举。指定 C++ 中 Word 文档节点的类型。"
type: docs
weight: 102000
url: /zh/cpp/aspose.words/nodetype/
---
## NodeType enum


指定 Word 文档节点的类型。

```cpp
enum class NodeType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Any | 0 | 表示所有节点类型。允许选择所有子节点。 |
| Document | 1 | 一个 [Document](../document/) 对象，作为文档树的根，提供对整个 Word 文档的访问。一个 [Document](../document/) 节点可以包含 [Section](../section/) 节点。 |
| Section | 2 | 一个对应于 Word 文档中一个章节的 [Section](../section/) 对象。一个 [Section](../section/) 节点可以包含 [Body](../body/) 和 [HeaderFooter](../headerfooter/) 节点。 |
| Body | 3 | 一个包含章节主体文本（主文本流）的 [Body](../body/) 对象。一个 [Body](../body/) 节点可以包含 [Paragraph](../paragraph/) 和 [Table](../../aspose.words.tables/table/) 节点。 |
| HeaderFooter | 4 | 一个包含章节中特定页眉或页脚文本的 [HeaderFooter](../headerfooter/) 对象。一个 [HeaderFooter](../headerfooter/) 节点可以包含 [Paragraph](../paragraph/) 和 [Table](../../aspose.words.tables/table/) 节点。 |
| Table | 5 | 一个表示 Word 文档中表格的 [Table](../../aspose.words.tables/table/) 对象。一个 [Table](../../aspose.words.tables/table/) 节点可以包含 [Row](../../aspose.words.tables/row/) 节点。 |
| Row | 6 | 表格的一行。一个 [Row](../../aspose.words.tables/row/) 节点可以包含 [Cell](../../aspose.words.tables/cell/) 节点。 |
| Cell | 7 | 表格行中的一个单元格。一个 [Cell](../../aspose.words.tables/cell/) 节点可以包含 [Paragraph](../paragraph/) 和 [Table](../../aspose.words.tables/table/) 节点。 |
| Paragraph | 8 | 一段文本。一个 [Paragraph](../paragraph/) 节点是用于内联级别元素的容器，包括 [Run](../run/)、[FieldStart](../../aspose.words.fields/fieldstart/)、[FieldSeparator](../../aspose.words.fields/fieldseparator/)、[FieldEnd](../../aspose.words.fields/fieldend/)、[FormField](../../aspose.words.fields/formfield/)、[Shape](../../aspose.words.drawing/shape/)、[GroupShape](../../aspose.words.drawing/groupshape/)、[Footnote](../../aspose.words.notes/footnote/)、[Comment](../comment/)、[SpecialChar](../specialchar/)，以及 [BookmarkStart](../bookmarkstart/) 和 [BookmarkEnd](../bookmarkend/)。 |
| BookmarkStart | 9 | 书签标记的开始。 |
| BookmarkEnd | 10 | 书签标记的结束。 |
| EditableRangeStart | 11 | 可编辑范围的开始。 |
| EditableRangeEnd | 12 | 可编辑范围的结束。 |
| MoveFromRangeStart | 13 | MoveFrom 范围的开始。 |
| MoveFromRangeEnd | 14 | MoveFrom 范围的结束。 |
| MoveToRangeStart | 15 | MoveTo 范围的开始。 |
| MoveToRangeEnd | 16 | MoveTo 范围的结束。 |
| GroupShape | 17 | 一组形状、图像、OLE 对象或其他组形状。一个 [GroupShape](../../aspose.words.drawing/groupshape/) 节点可以包含其他 [Shape](../../aspose.words.drawing/shape/) 和 [GroupShape](../../aspose.words.drawing/groupshape/) 节点。 |
| Shape | 18 | 绘图对象，例如 OfficeArt 形状、图像或 OLE 对象。一个 [Shape](../../aspose.words.drawing/shape/) 节点可以包含 [Paragraph](../paragraph/) 和 [Table](../../aspose.words.tables/table/) 节点。 |
| Comment | 19 | Word 文档中的批注。一个 [Comment](../comment/) 节点可以拥有 [Paragraph](../paragraph/) 和 [Table](../../aspose.words.tables/table/) 节点。 |
| Footnote | 20 | Word 文档中的脚注或尾注。一个 [Footnote](../../aspose.words.notes/footnote/) 节点可以拥有 [Paragraph](../paragraph/) 和 [Table](../../aspose.words.tables/table/) 节点。 |
| 运行 | 21 | 一段文本。 |
| FieldStart | 22 | 用于指示 Word 域开始的特殊字符。 |
| FieldSeparator | 23 | 用于将域代码与域结果分隔开的特殊字符。 |
| FieldEnd | 24 | 用于标识 Word 字段结束的特殊字符。 |
| FormField | 25 | 表单字段。 |
| SpecialChar | 26 | 不是更具体的特殊字符类型之一的特殊字符。 |
| SmartTag | 27 | 段落中围绕一个或多个内联结构（运行、图像、字段等）的智能标签。 |
| StructuredDocumentTag | 28 | 允许定义客户特定信息及其呈现方式。 |
| StructuredDocumentTagRangeStart | 29 | **ranged** 结构化文档标签的开始，接受多节内容。 |
| StructuredDocumentTagRangeEnd | 30 | **ranged** 结构化文档标签的结束，接受多节内容。 |
| GlossaryDocument | 31 | 主文档中的词汇表文档。 |
| BuildingBlock | 32 | 词汇表文档中的构建块（例如词汇表文档条目）。 |
| CommentRangeStart | 33 | 表示注释范围开始的标记节点。 |
| CommentRangeEnd | 34 | 表示注释范围结束的标记节点。 |
| OfficeMath | 35 | Office [Math](../../aspose.words.math/) 对象。可以是方程式、函数、矩阵或其他数学对象之一。它可以是数学对象的集合，也可以包含一些非数学对象，例如文本运行。 |
| SubDocument | 36 | 一个子文档节点，它是指向另一个文档的链接。 |
| System | 37 | 供 [Aspose.Words](../) 内部使用保留。 |
| Null | 38 | 供 [Aspose.Words](../) 内部使用保留。 |


## 示例



展示如何遍历复合节点的子节点集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 向本文档的第一段添加两个运行和一个形状作为子节点。
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// 请注意，'CustomNodeId' 不会保存到输出文件中，仅在节点生命周期内存在。
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// 遍历段落的直接子节点集合，
// 并打印我们在其中找到的任何运行或形状。
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
