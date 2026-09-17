---
title: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions méthode"
linktitle: "get_AdvancedOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions méthode. Spécifie des options de comparaison avancées qui peuvent aider à produire une sortie de comparaison plus précise en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


Spécifie des options de comparaison avancées qui peuvent aider à produire une sortie de comparaison plus précise.

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
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

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
