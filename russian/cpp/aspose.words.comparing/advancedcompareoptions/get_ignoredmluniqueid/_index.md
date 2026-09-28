---
title: "Метод Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId"
linktitle: "get_IgnoreDmlUniqueId"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId. Указывает, следует ли игнорировать различия в уникальном идентификаторе DrawingML в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.comparing/advancedcompareoptions/get_ignoredmluniqueid/
---
## AdvancedCompareOptions::get_IgnoreDmlUniqueId method


Указывает, следует ли игнорировать различия в уникальном идентификаторе DrawingML.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId() const
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

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
