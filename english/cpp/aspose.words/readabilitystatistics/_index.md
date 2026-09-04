---
title: Aspose::Words::ReadabilityStatistics class
linktitle: ReadabilityStatistics
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ReadabilityStatistics class. Provides information about document readability score in C++.'
type: docs
weight: 51500
url: /cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


Provides information about document readability score.

```cpp
class ReadabilityStatistics : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Flesch-Kincaid Grade Level score. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Flesch Reading Easy score. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Examples



Shows how to calculate and display the Flesch reading scores for a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Calculate readability statistics.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// Verify that the scores are within expected valid ranges.
// CSPORTCPP: Unsupported expression type Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
