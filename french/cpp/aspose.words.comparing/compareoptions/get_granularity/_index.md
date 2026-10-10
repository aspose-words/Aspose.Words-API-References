---
title: "Aspose::Words::Comparing::CompareOptions::get_Granularity méthode"
linktitle: "get_Granularity"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comparing::CompareOptions::get_Granularity méthode. Spécifie si les modifications sont suivies par caractère ou par mot en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions::get_Granularity method


Spécifie si les modifications sont suivies par caractère ou par mot.

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


## Exemples



Montre comment spécifier une granularité lors de la comparaison de documents.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Spécifiez si les modifications sont suivies
// par caractère ('Granularity.CharLevel'), ou par mot ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// La collection de groupes de révisions du premier document contient toutes les différences entre les documents.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## Voir aussi

* Enum [Granularity](../../granularity/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
