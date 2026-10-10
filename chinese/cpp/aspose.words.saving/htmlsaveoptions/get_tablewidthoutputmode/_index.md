---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode 方法"
linktitle: "get_TableWidthOutputMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode 方法。控制表格、行和单元格宽度导出到 HTML、MHTML 或 EPUB 的方式。默认值在 C++ 中为 All。"
type: docs
weight: 47000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


控制表格、行和单元格宽度导出到 HTML、MHTML 或 EPUB 的方式。默认值为 [All](../../htmlelementsizeoutputmode/)。

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## 备注


在 HTML 格式中，表格、行和单元格元素（**%<table>**、**%<tr>**、**%<th>**、**%<td>**）的宽度可以以相对（百分比）或绝对单位指定。在 Aspose.Words 文档中，表格、行和单元格的宽度也可以使用相对或绝对单位指定。

当使用 Aspose.Words 将文档转换为 HTML 时，您可能希望控制表格、行和单元格宽度的导出方式，以影响生成的文档在可视化代理（例如浏览器或查看器）中的显示效果。

将此属性用作过滤器，以指定哪些表格宽度值会导出到目标文档。例如，如果您将文档转换为 EPUB 并打算在移动阅读设备上查看，则可能希望避免导出绝对宽度值。为此，您需要将输出模式指定为 [RelativeOnly](../../htmlelementsizeoutputmode/) 或 [None](../../htmlelementsizeoutputmode/)，以便移动设备上的查看器能够尽可能将表格布局为适应屏幕宽度。

## 示例



展示如何在输出的 .html 中保留负缩进。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个带负缩进的表格，它会将表格向左推至左页边界之外。
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// 插入一个带正缩进的表格，它会将表格向右推移。
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// 当我们将文档保存为 HTML 时，Aspose.Words 只会保留负缩进
// 例如，如果我们设置 "AllowNegativeIndent" 标志，就会对第一个表格应用此负缩进。
// 在我们将其设置为 "true" 的 SaveOptions 对象中。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## 另见

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
