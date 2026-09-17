---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId méthode"
linktitle: "get_IgnoreStoreItemId"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId méthode. Spécifie s'il faut ignorer la différence dans l'ID d'élément de stockage StructuredDocumentTag en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


Spécifie s'il faut ignorer la différence dans l'ID de l'élément de stockage StructuredDocumentTag.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## Exemples



Montre comment comparer des SDT avec le même contenu mais un ID d'élément de stockage différent.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Configurez les options pour comparer des SDT avec le même contenu mais un ID d'élément de stockage différent.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Voir aussi

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
