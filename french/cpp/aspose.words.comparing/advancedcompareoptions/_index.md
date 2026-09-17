---
title: "Aspose::Words::Comparing::AdvancedCompareOptions classe"
linktitle: "AdvancedCompareOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions classe. Permet de définir des options de comparaison avancées en C++."
type: docs
weight: 500
url: /fr/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


Permet de définir des options de comparaison avancées.

```cpp
class AdvancedCompareOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | Spécifie s'il faut ignorer la différence dans l'ID unique de DrawingML. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | Spécifie s'il faut ignorer la différence dans l'ID de l'élément de stockage StructuredDocumentTag. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Mutateur pour [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | Mutateur pour [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
