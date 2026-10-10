---
title: "Aspose::Words::CompositeNode::GetChildNodes 方法"
linktitle: "GetChildNodes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode::GetChildNodes 方法。返回在 C++ 中匹配指定类型的子节点的实时集合。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/compositenode/getchildnodes/
---
## CompositeNode::GetChildNodes method


返回匹配指定类型的子节点的实时集合。

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::CompositeNode::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | 指定要选择的节点类型。 |
| isDeep | bool | **true** 用于递归选择所有子节点；**false** 用于仅在直接子节点中选择。 |

### ReturnValue

指定类型的子节点的实时集合。
## 备注


此方法返回的节点集合始终是实时的。

实时集合始终与文档保持同步。例如，如果您选择文档中的所有章节并遍历集合删除这些章节，则当章节从文档中删除时，它会立即从集合中移除。

## 示例



展示如何打印文档的所有评论及其回复。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// 如果评论没有父级，则它是"顶层"评论，而不是回复类型的评论。
// 打印所有顶层评论以及它们可能拥有的任何回复。
for (auto&& comment : comments->LINQ_OfType<System::SharedPtr<Aspose::Words::Comment> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Comment>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Comment> c)>>([](System::SharedPtr<Aspose::Words::Comment> c) -> bool
{
    return c->get_Ancestor() == nullptr;
})))->LINQ_ToList())
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\", by {1}", comment->GetText().Trim(), comment->get_Author()) << std::endl;
    std::cout << System::String::Format(u"Has {0} replies", comment->get_Replies()->get_Count()) << std::endl;
    for (auto&& commentReply : System::IterateOver<Aspose::Words::Comment>(comment->get_Replies()))
    {
        std::cout << System::String::Format(u"\t\"{0}\", by {1}", commentReply->GetText().Trim(), commentReply->get_Author()) << std::endl;
    }
    std::cout << std::endl;
}
```


展示如何从文档中提取图像，并将它们保存为本地文件系统中的单独文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// 从文档中获取形状集合，
// 并将每个包含图像的形状的图像数据保存为本地文件系统中的文件。
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // 形状的图像数据可能包含多种可能的图像格式。
        // 我们可以根据图像的格式自动确定每个图像的文件扩展名。
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


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


展示如何在 [CompositeNode](../) 的子节点集合中添加、更新和删除子节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 默认情况下，空文档只有一个段落。
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// 复合节点（例如我们的段落）可以包含其他复合节点和内联节点作为子节点。
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// 创建另外三个运行节点。
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// 文档主体在我们将这些运行插入到复合节点之前不会显示它们
// 该复合节点本身是文档节点树的一部分，就像我们对第一个运行所做的那样。
// 我们可以确定插入的节点的文本内容位于何处
// 通过相对于段落中另一个节点指定插入位置，来决定它在文档中的出现位置。
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// 将第二个运行插入到段落中，位于初始运行之前。
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// 在初始运行之后插入第三个运行。
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// 将第一个运行插入到段落子节点集合的开头。
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 我们可以通过编辑和删除现有子节点来修改运行的内容。
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## 另见

* Class [NodeCollection](../../nodecollection/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
