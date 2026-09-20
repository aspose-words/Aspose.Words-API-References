---
title: "Aspose::Words::Document::get_ReadabilityStatistics метод"
linktitle: "get_ReadabilityStatistics"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_ReadabilityStatistics метод. Предоставляет информацию о показателях читаемости документа в C++."
type: docs
weight: 44750
url: /ru/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


Предоставляет информацию о показателе читаемости документа.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


## Примеры



Показывает, как вычислить и отобразить оценки чтения Флеша для документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Вычислить статистику читаемости.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// Проверьте, что оценки находятся в ожидаемых допустимых диапазонах.
// CSPORTCPP: Неподдерживаемый тип выражения Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## См. также

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
