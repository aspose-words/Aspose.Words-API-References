---
title: "Aspose::Words::ParagraphFormat::get_LineSpacing 方法"
linktitle: "get_LineSpacing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_LineSpacing 方法。获取或设置段落的行距（以点为单位），在 C++ 中。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words/paragraphformat/get_linespacing/
---
## ParagraphFormat::get_LineSpacing method


获取或设置段落的行距（以点为单位）。

```cpp
double Aspose::Words::ParagraphFormat::get_LineSpacing()
```

## 备注


当 [LineSpacingRule](../get_linespacingrule/) 属性设置为 [AtLeast](../../linespacingrule/) 时，行距可以大于或等于指定的 [LineSpacing](./) 值，但永不小于该值。

当 [LineSpacingRule](../get_linespacingrule/) 属性设置为 [Exactly](../../linespacingrule/) 时，行距永不偏离指定的 [LineSpacing](./) 值，即使段落中使用了更大的字体。

## 示例



展示如何使用行间距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是我们可以使用的三种行间距规则
// 段落的 "LineSpacingRule" 属性来配置段落之间的间距。
// 1 - 设置最小间距。
// 这将为任意大小的文本行提供垂直填充
// 如果太小，将无法保持最小行高。
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 - 设置精确间距。
// 使用超出间距的过大字体大小会导致文本被截断。
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 - 将间距设置为默认行间距的倍数，默认情况下为 12 点。
// 此类间距会随不同的字体大小而缩放。
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
