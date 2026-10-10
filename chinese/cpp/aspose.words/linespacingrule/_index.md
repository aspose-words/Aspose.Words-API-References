---
title: "Aspose::Words::LineSpacingRule enum"
linktitle: "LineSpacingRule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LineSpacingRule enum. 指定 C++ 中段落的行间距值。"
type: docs
weight: 95000
url: /zh/cpp/aspose.words/linespacingrule/
---
## LineSpacingRule enum


指定段落的行距值。

```cpp
enum class LineSpacingRule
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| AtLeast | 0 | 行间距可以大于或等于，但永不小于在 [LineSpacing](../paragraphformat/get_linespacing/) 属性中指定的值。 |
| Exactly | 1 | 即使段落中使用了更大的字体，行间距也永远不会改变，始终保持在 [LineSpacing](../paragraphformat/get_linespacing/) 属性中指定的值。 |
| Multiple | 2 | 行间距在 [LineSpacing](../paragraphformat/get_linespacing/) 属性中以行数指定。1 行等于 12 点。 |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
