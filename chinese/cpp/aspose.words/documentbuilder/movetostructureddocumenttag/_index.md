---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag 方法"
linktitle: "MoveToStructuredDocumentTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag 方法。将在 C++ 中将光标移动到结构化文档标签。"
type: docs
weight: 61000
url: /zh/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


将光标移动到结构化文档标签。

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\& | 要移动到的结构化文档标签。 |
| characterIndex | int32_t | 结构化文档标签内字符的索引。负值允许您指定相对于结构化文档标签末尾的位置。使用 -1 可移动到结构化文档标签的末尾。如果结构化文档标签位于块级别，并且您想将光标移动到其最后一个段落的末尾，请指定 -2。 |

## 示例



展示如何使用 [DocumentBuilder](../) 将光标移动到结构化文档标签内部。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 有多种方式可以移动光标：
// 1 -  通过索引移动到结构化文档标签的第一个字符。
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  通过对象移动到结构化文档标签的第一个字符。
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  移动到第二个结构化文档标签的末尾。
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// 获取当前选中的结构化文档标签。
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## 另见

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


将光标移动到当前节中的结构化文档标签。

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | 要移动到的结构化文档标签的索引。 |
| characterIndex | int32_t | 结构化文档标签内字符的索引。负值允许您指定相对于结构化文档标签末尾的位置。使用 -1 可移动到结构化文档标签的末尾。如果结构化文档标签位于块级别，并且您想将光标移动到其最后一个段落的末尾，请指定 -2。 |
## 备注


导航在当前章节的当前故事内部执行。也就是说，如果您将光标移动到第一节的主页眉，则 *structuredDocumentTagIndex* 指定该节页眉中结构化文档标签的索引。

当 *structuredDocumentTagIndex* 大于或等于 0 时，它表示从章节开头算起的索引，0 表示第一个结构化文档标签。当 *structuredDocumentTagIndex* 小于 0 时，它表示从章节末尾算起的索引，-1 表示最后一个结构化文档标签。

## 示例



展示如何使用 [DocumentBuilder](../) 将光标移动到结构化文档标签内部。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 有多种方式可以移动光标：
// 1 -  通过索引移动到结构化文档标签的第一个字符。
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  通过对象移动到结构化文档标签的第一个字符。
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  移动到第二个结构化文档标签的末尾。
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// 获取当前选中的结构化文档标签。
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
