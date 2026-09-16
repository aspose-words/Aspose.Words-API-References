---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph 方法"
linktitle: "MoveToParagraph"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph 方法。将光标移动到当前章节中的段落（C++）。"
type: docs
weight: 59000
url: /zh/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


将光标移动到当前节中的段落。

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| paragraphIndex | int32_t | 要移动到的段落索引。 |
| characterIndex | int32_t | 段落内字符的索引。负值可用于指定从段落末尾开始的位置。使用 -1 可移动到段落的末尾。 |
## 备注


导航在当前章节的当前故事内部执行。也就是说，如果将光标移动到第一章节的主标题，则 *paragraphIndex* 指定该章节该标题内段落的索引。

当 *paragraphIndex* 大于或等于 0 时，它表示从章节开头算起的索引，0 为第一段。当 *paragraphIndex* 小于 0 时，它表示从章节末尾算起的索引，-1 为最后一段。

## 示例



展示如何将构建器的光标位置移动到指定段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// 创建文档构建器以编辑文档。构建器的光标，
// 它是我们调用文档构建方法时插入新节点的位置，
// 当前位于文档的开头。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// 将该光标移动到其他段落会将光标放置在该段落前面。
builder->MoveToParagraph(2, 0);

// 我们添加的任何新内容都会插入到该位置。
builder->Writeln(u"This is a new third paragraph. ");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
