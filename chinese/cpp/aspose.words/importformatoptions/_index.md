---
title: "Aspose::Words::ImportFormatOptions 类"
linktitle: "ImportFormatOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions 类。允许指定各种导入选项以格式化输出。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 35000
url: /zh/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


允许指定各种导入选项以格式化输出。要了解更多，请访问 [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) 文档文章。

```cpp
class ImportFormatOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | 获取或设置一个布尔值，指定是否自动调整句子和单词间距。默认值为 **false**。 |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | 获取或设置一个布尔值，指示在调用 [AppendDocument()](../) 时是否强制将首个导入的章节类型更改为 [NewPage](../sectionstart/)。默认值为 **true**。 |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | 获取或设置一个布尔值，指示是否在 [KeepSourceFormatting](../importformatmode/) 模式下复制冲突的样式。默认值为 **false**。 |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | 获取或设置一个布尔值，指定在使用 [KeepSourceFormatting](../importformatmode/) 模式时忽略页眉/页脚内容的源格式。默认值为 **true**。 |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | 获取或设置一个布尔值，指定如果使用 [KeepSourceFormatting](../importformatmode/) 模式，则忽略文本框内容的源格式。默认值为 **true**。 |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | 获取或设置一个布尔值，指定当源文档和目标文档的编号冲突时，编号的导入方式。默认值为 **false**。 |
| [get_MergePastedLists](./get_mergepastedlists/)() const | 获取或设置一个布尔值，指定粘贴的列表是否会与周围的列表合并。默认值为 **false**。 |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | 获取或设置一个布尔值，指定是否强制解析形状的主题颜色。默认值为 **false**。 |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | 获取或设置一个布尔值，指定当源文档和目标文档的样式名称相同且冲突时，样式的导入方式。默认值为 **false**。 |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/) 的 setter。 |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/) 的 setter。 |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/) 的 setter。 |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/) 的 setter。 |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/) 的 setter。 |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/) 的 setter。 |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/) 的 setter。 |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/) 的 setter。 |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | 用于 [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示在插入文档时如何解决重复样式。
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// 克隆文档并编辑克隆的 "MyStyle" 样式，使其颜色与原始文档不同。
// 如果我们将克隆插入原始文档，两个同名样式将导致冲突。
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// 当我们启用 SmartStyleBehavior 并使用 KeepSourceFormatting 导入格式模式时，
// Aspose.Words 将通过转换源文档的样式来解决样式冲突。
// 将与目标样式同名的样式转换为直接的段落属性。
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
