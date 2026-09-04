---
title: Aspose::Words::Document::get_ReadabilityStatistics method
linktitle: get_ReadabilityStatistics
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_ReadabilityStatistics method. Provides readability score information for the document in C++.'
type: docs
weight: 44750
url: /cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


Provides readability score information for the document.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


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

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
