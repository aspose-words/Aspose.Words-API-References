---
title: "Aspose::Words::Comment::AddReply 方法"
linktitle: "AddReply"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment::AddReply 方法。在 C++ 中向此评论添加回复。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/comment/addreply/
---
## Comment::AddReply method


向此评论添加回复。

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::AddReply(const System::String &author, const System::String &initial, System::DateTime dateTime, const System::String &text)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 作者 | const System::String\& | 回复的作者名称。 |
| initial | const System::String\& | 回复的作者缩写。 |
| dateTime | System::DateTime | 回复的日期和时间。 |
| 文本 | const System::String\& | 回复文本。 |

### ReturnValue

为回复创建的 [Comment](../) 节点。
## 备注


由于现有的 MS Office 限制，文档中仅允许 1 级回复。

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
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
