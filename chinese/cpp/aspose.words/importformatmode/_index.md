---
title: "Aspose::Words::ImportFormatMode 枚举"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatMode 枚举。指定在 C++ 中从另一个文档导入内容时如何合并格式。"
type: docs
weight: 93000
url: /zh/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


指定从另一个文档导入内容时格式的合并方式。

```cpp
enum class ImportFormatMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| UseDestinationStyles | 0 | 使用目标文档的样式并复制新样式。这是默认选项。 |
| KeepSourceFormatting | 1 | 将所有必需的样式复制到目标文档，如有需要生成唯一的样式名称。 |
| KeepDifferentStyles | 2 | 仅复制与源文档中不同的样式。 |

## 备注


当您将节点从一个文档复制到另一个文档时，此选项指定当两个文档拥有同名但格式不同的样式时，如何解析格式。

格式解析如下：

1. 内置样式使用其与语言环境无关的样式标识符进行匹配。用户定义的样式使用区分大小写的样式名称进行匹配。
1. 如果在目标文档中未找到匹配的样式，则将该样式（以及其引用的所有样式）复制到目标文档，并将导入的节点更新为引用新样式。
1. 如果目标文档中已存在匹配的样式，则其行为取决于传递给 [ImportNode()](../) 的 **importFormatMode** 参数，如下所述。



使用 [UseDestinationStyles](./) 选项时，如果目标文档中已存在匹配的样式，则不会复制该样式，导入的节点将更新为引用已有的样式。

使用 [UseDestinationStyles](./) 的缺点是，导入的文本在目标文档中可能看起来与源文档不同。例如，源文档中的 “Heading 1” 样式使用 Arial 16pt 字体，而目标文档中的 “Heading 1” 样式使用 Times New Roman 14pt 字体。当导入没有其他直接格式的 “Heading 1” 样式文本时，它将在目标文档中显示为 Times New Roman 14pt 字体。

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

使用 [KeepSourceFormatting](./) 的缺点是，如果进行多次导入，目标文档中可能会出现大量样式，这会使在 Microsoft Word 中对该文档使用一致的样式格式变得困难。

使用 [KeepDifferentStyles](./) 选项可以在目标样式提供的格式与源文档中的样式完全相同的情况下复用目标样式。如果目标文档中的样式与源文档不同，则会进行导入。

## 示例



展示如何将一个文档插入到另一个文档中。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
