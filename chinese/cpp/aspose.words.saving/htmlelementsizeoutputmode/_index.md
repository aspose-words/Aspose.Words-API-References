---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode 枚举"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode 枚举。指定 Aspose.Words 在 C++ 中如何将元素宽度和高度导出到 HTML、MHTML 和 EPUB。"
type: docs
weight: 58000
url: /zh/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


指定 Aspose.Words 如何将元素的宽度和高度导出为 HTML、MHTML 和 EPUB。

```cpp
enum class HtmlElementSizeOutputMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 全部 | 0 | 文档中指定的所有元素尺寸，无论是绝对单位还是相对单位，都会被导出。 |
| RelativeOnly | 1 | 仅当文档中以相对单位指定时，元素尺寸才会被导出。固定尺寸在此模式下不会导出。可视化代理将计算缺失的尺寸，以使文档布局更自然。 |
| None | 2 | 元素尺寸不会被导出。可视化代理将根据元素之间的关系自动构建布局。 |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
