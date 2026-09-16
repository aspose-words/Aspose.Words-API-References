---
title: "Aspose::Words::NodeImporter::NodeImporter 构造函数"
linktitle: "NodeImporter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeImporter::NodeImporter 构造函数。初始化 NodeImporter 类的新实例，使用 C++。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


初始化 [NodeImporter](../) 类的新实例。

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 源文档。 |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 将成为导入节点所有者的目标文档。 |
| importFormatMode | Aspose::Words::ImportFormatMode | 指定如何合并冲突的样式格式。 |

## 另见

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


初始化 [NodeImporter](../) 类的新实例。

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 源文档。 |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 将成为导入节点所有者的目标文档。 |
| importFormatMode | Aspose::Words::ImportFormatMode | 指定如何合并冲突的样式格式。 |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | 指定用于格式化导入节点的各种选项。 |

## 示例



展示在导入具有相同列表定义标识符的列表时如何解决冲突。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// 将 "KeepSourceNumbering" 属性设置为 "true" 以应用不同的列表定义 ID
// 到与 Aspose.Words 将其导入目标文档时相同的样式。
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


展示如何解决源文档和目标文档中的列表编号冲突。
```cpp
// 打开一个具有自定义列表编号方案的文档，然后克隆它。
// 由于两者具有相同的编号格式，如果我们将一个文档导入另一个文档，格式将会冲突。
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// 当我们将文档的克隆导入到原始文档中并随后追加它时，
// 那么具有相同列表格式的两个列表将会合并。
// 如果我们将 "KeepSourceNumbering" 标志设置为 "false"，则来自文档克隆的列表
// 我们追加到原始文档的列表将继续使用我们追加到的列表的编号。
// 这将有效地将两个列表合并为一个。
// 如果我们将 "KeepSourceNumbering" 标志设置为 "true"，则文档克隆
// 列表将保留其原始编号，使两个列表显示为独立的列表。
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    System::SharedPtr<Aspose::Words::Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Node>>(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" + u"12. Item 3\r\n" + u"13. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
```

## 另见

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
