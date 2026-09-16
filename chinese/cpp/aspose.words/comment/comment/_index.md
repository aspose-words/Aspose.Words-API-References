---
title: "Aspose::Words::Comment::Comment 构造函数"
linktitle: "Comment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment::Comment 构造函数。初始化 Comment 类在 C++ 中的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


初始化 [Comment](../) 类的新实例。

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 所属文档。 |
## 备注


当创建 [Comment](../) 时，它属于指定的文档，但尚未成为文档的一部分，并且 [ParentNode](../../node/get_parentnode/) 为 **null**。

要将 [Comment](../) 追加到文档中，请在希望插入评论的段落上使用 [InsertAfter1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)\">InsertBefore1()](../)。

创建评论后，别忘了设置其 [Author](../get_author/)、[Initial](../get_initial/) 和 [DateTime](../get_datetime/) 属性。

## 另见

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


初始化 [Comment](../) 类的新实例。

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 所属文档。 |
| 作者 | const System::String\& | 评论的作者名称。不能为 **null**。 |
| initial | const System::String\& | 评论的作者首字母。不能为 **null**。 |
| dateTime | System::DateTime | 评论的日期和时间。 |

## 示例



展示如何向段落添加评论。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// 在 Microsoft Word 中，我们可以右键单击文档正文中的此评论进行编辑或回复。
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## 另见

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
