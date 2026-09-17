---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId méthode"
linktitle: "get_IgnoreDmlUniqueId"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId méthode. Spécifie si l'on doit ignorer la différence dans l'identifiant unique DrawingML en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.comparing/advancedcompareoptions/get_ignoredmluniqueid/
---
## AdvancedCompareOptions::get_IgnoreDmlUniqueId method


Spécifie s'il faut ignorer la différence dans l'ID unique de DrawingML.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId() const
```


## Exemples



Montre comment comparer des documents en ignorant l'ID unique DML.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// Par défaut, Aspose.Words n'ignore pas l'ID unique du DML, et le nombre de révisions était de 2.
// Si nous ignorons l'ID unique du DML, le nombre de révisions était de 0.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## Voir aussi

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
