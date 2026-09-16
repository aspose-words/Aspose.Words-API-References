---
title: "Aspose::Words::Document::get_ReadabilityStatistics 方法"
linktitle: "get_ReadabilityStatistics"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_ReadabilityStatistics 方法。提供文档在 C++ 中的可读性评分信息。"
type: docs
weight: 44750
url: /zh/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


提供文档的可读性评分信息。

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


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

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
