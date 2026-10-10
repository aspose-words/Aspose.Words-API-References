---
title: "Aspose::Words::ReadabilityStatistics 类"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ReadabilityStatistics 类。提供有关 C++ 中文档可读性评分的信息。"
type: docs
weight: 51500
url: /zh/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


提供有关文档可读性评分的信息。

```cpp
class ReadabilityStatistics : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Flesch-Kincaid 年级水平分数。 |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Flesch 阅读易度分数。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 示例



展示如何计算并显示文档的 Flesch 阅读分数。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// 计算可读性统计信息。
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// 验证这些分数是否在预期的有效范围内。
// CSPORTCPP: 不支持的表达式类型 Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
