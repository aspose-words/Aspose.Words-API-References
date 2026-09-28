---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId метод"
linktitle: "get_IgnoreStoreItemId"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId метод. Указывает, следует ли игнорировать различия в идентификаторе хранилища StructuredDocumentTag в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


Указывает, следует ли игнорировать различия в идентификаторе элемента хранилища StructuredDocumentTag.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## Примеры



Показывает, как сравнить SDT с одинаковым содержимым, но разным идентификатором элемента хранилища.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Настройте параметры для сравнения SDT с одинаковым содержимым, но разным идентификатором элемента хранилища.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## См. также

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
