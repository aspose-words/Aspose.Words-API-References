---
title: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering 方法"
linktitle: "get_KeepSourceNumbering"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering 方法。获取或设置一个布尔值，用于指定当源文档和目标文档中的编号冲突时，编号将如何导入。默认值在 C++ 中为 false。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/importformatoptions/get_keepsourcenumbering/
---
## ImportFormatOptions::get_KeepSourceNumbering method


获取或设置一个布尔值，指定当源文档和目标文档的编号冲突时，编号的导入方式。默认值为 **false**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering() const
```


## 示例



展示如何导入带编号列表的文档。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

ASSERT_EQ(4, dstDoc->get_Lists()->get_Count());

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();

// 如果出现列表样式冲突，则应用源文档的列表格式。
// 将 \"KeepSourceNumbering\" 属性设置为 \"false\"，以不将任何列表编号导入目标文档。
// 将 \"KeepSourceNumbering\" 属性设置为 \"true\"，导入所有冲突的
// 列表样式编号保持与源文档中相同的外观。
options->set_KeepSourceNumbering(isKeepSourceNumbering);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);
dstDoc->UpdateListLabels();

ASSERT_EQ(isKeepSourceNumbering ? 5 : 4, dstDoc->get_Lists()->get_Count());
```


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

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
