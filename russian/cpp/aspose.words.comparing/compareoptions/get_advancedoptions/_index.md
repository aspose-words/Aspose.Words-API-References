---
title: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions метод"
linktitle: "get_AdvancedOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions метод. Указывает расширенные параметры сравнения, которые могут помочь получить более точный результат сравнения в C++."
type: docs
weight: 2500
url: /ru/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


Указывает расширенные параметры сравнения, которые могут помочь получить более точный результат сравнения.

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
```


## Примеры



Показывает, как сравнивать документы, игнорируя уникальный идентификатор DML.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// По умолчанию Aspose.Words не игнорирует уникальный идентификатор DML, и количество правок было 2.
// Если мы игнорируем уникальный идентификатор DML, количество правок будет 0.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## См. также

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
