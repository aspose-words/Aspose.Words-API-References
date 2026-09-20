---
title: "Aspose::Words::NodeImporter 类"
linktitle: "NodeImporter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeImporter 类。允许高效地将节点从一个文档重复导入到另一个文档。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 44000
url: /zh/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


允许高效地重复将节点从一个文档导入到另一个文档。要了解更多，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class NodeImporter : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | 将节点从一个文档导入到另一个文档中。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | 初始化 [NodeImporter](./) 类的新实例。 |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | 初始化 [NodeImporter](./) 类的新实例。 |
| static [Type](./type/)() |  |
## 备注


Aspose.Words 提供了在 Microsoft Word 文档之间轻松复制和移动片段的功能。这被称为 "importing nodes"。在您可以将片段从一个文档插入到另一个文档之前，需要先 "import" 它。导入会创建原始节点的深度克隆，准备插入到目标文档中。

导入节点的最简单方法是使用 [DocumentBase](../documentbase/) 对象提供的 [ImportNode()](../) 方法。

然而，当您需要多次将节点从一个文档导入到另一个文档时，最好使用 [NodeImporter](./) 类。[NodeImporter](./) 类可以最大限度地减少在目标文档中创建的样式和列表数量。

在 Microsoft Word 文档之间复制或移动片段会给 Aspose.Words 带来许多技术挑战。在 Word 文档中，样式和列表格式是集中存储的，独立于文档的文本。段落和文本运行仅通过内部唯一标识符引用这些样式。

这些挑战源于不同文档中的样式和列表各不相同。例如，要将使用 Heading 1 样式格式化的段落从一个文档复制到另一个文档，需要考虑多项因素：决定是否将 Heading 1 样式从源文档复制到目标文档，克隆段落，更新克隆后的段落，使其引用目标文档中正确的 Heading 1 样式。如果必须复制该样式，还需分析并可能复制它所引用的所有样式（基于样式和下一段落样式），依此类推。由于 Microsoft Word 将列表定义独立于文本存储，复制项目符号或编号段落时也会出现类似问题。

[NodeImporter](./) 类类似于一个上下文，在导入期间保存“translation tables”。它能够在源文档和目标文档之间正确地转换样式和列表。

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
