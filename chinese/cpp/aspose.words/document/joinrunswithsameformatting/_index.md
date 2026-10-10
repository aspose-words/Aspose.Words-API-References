---
title: "Aspose::Words::Document::JoinRunsWithSameFormatting 方法"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::JoinRunsWithSameFormatting 方法。将在 C++ 中文档所有段落中具有相同格式的运行合并。"
type: docs
weight: 65000
url: /zh/cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


合并文档中所有段落中具有相同格式的运行。

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

已执行的合并次数。当 **N** 个相邻的运行被合并时，它们计为 **N - 1** 次合并。
## 备注


这是一种优化方法。某些文档包含具有相同格式的相邻运行。通常在文档被手动大量编辑时会出现这种情况。通过合并这些运行，您可以减小文档大小并加快后续处理速度。

该操作检查文档中每个 [Paragraph](../../paragraph/) 节点，寻找具有相同属性的相邻 [Run](../../run/) 节点。它会忽略用于跟踪运行创建和修改编辑会话的唯一标识符。每个合并序列中的第一个运行会累计所有文本。其余的运行将从文档中删除。

## 示例



展示如何在文档中合并运行以减少不必要的运行。
```cpp
// 打开一个包含具有相同格式的相邻文本运行的文档，
// 这通常发生在我们在 Microsoft Word 中多次编辑同一段落时。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 如果这些运行中的任意数量是相邻且具有相同的格式，
// 则文档可以被简化。
ASSERT_EQ(317, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());

// 使用此方法合并这些运行，并验证将要进行的运行合并次数。
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// 合并后我们拥有的合并次数和运行数量
// 应当等于我们最初的运行数量之和。
ASSERT_EQ(196, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
