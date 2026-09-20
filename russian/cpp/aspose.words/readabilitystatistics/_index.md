---
title: "Aspose::Words::ReadabilityStatistics class"
linktitle: "ReadabilityStatistics"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ReadabilityStatistics class. Предоставляет информацию о показателе читаемости документа в C++."
type: docs
weight: 51500
url: /ru/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


Предоставляет информацию о показателе читабельности документа.

```cpp
class ReadabilityStatistics : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Оценка уровня по шкале Флеша‑Кинкейда. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Оценка лёгкости чтения по Флешу. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
