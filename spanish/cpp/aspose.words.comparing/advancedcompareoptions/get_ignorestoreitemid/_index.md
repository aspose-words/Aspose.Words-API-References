---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId método"
linktitle: "get_IgnoreStoreItemId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId método. Especifica si se debe ignorar la diferencia en el Id de elemento almacenado de StructuredDocumentTag en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


Especifica si se debe ignorar la diferencia en el Id del elemento almacenado de StructuredDocumentTag.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## Ejemplos



Muestra cómo comparar SDT con el mismo contenido pero con un id de elemento almacenado diferente.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Configure opciones para comparar SDT con el mismo contenido pero con un id de elemento almacenado diferente.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Ver también

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
