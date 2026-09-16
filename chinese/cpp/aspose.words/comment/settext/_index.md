---
title: "Aspose::Words::Comment::SetText 方法"
linktitle: "SetText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment::SetText 方法。这是一个便利方法，允许在 C++ 中轻松设置评论的文本。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


这是一个便利方法，允许轻松设置评论的文本。

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文本 | const System::String\& | 评论的新文本。 |
## 备注


此方法允许从字符串快速设置评论的文本。字符串可以包含段落换行符，这将相应地在评论中创建文本段落。如果您想在评论中插入更复杂的元素，例如书签、表格或应用丰富的格式，则需要使用相应的节点类来构建评论文本。

## 示例



展示如何向文档添加评论，然后对其进行回复。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// 将评论放置在文档正文中的节点上。
// 此评论将显示在其段落的位置，
// 位于页面右侧边距之外，并且有一条虚线将其连接到段落。
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// 添加一个回复，该回复将显示在其父评论下方。
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// 评论和回复都是 Comment 节点。
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// 不回复其他评论的评论是“顶级”评论。它们没有上级评论。
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// 回复拥有一个上级顶级评论。
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## 另见

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
