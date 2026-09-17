---
title: "Aspose::Words::Comparing::Granularity énum"
linktitle: "Granularity"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comparing::Granularity énum. Spécifie la granularité des modifications à suivre lors de la comparaison de deux documents en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.comparing/granularity/
---
## Granularity enum


Spécifie la granularité des modifications à suivre lors de la comparaison de deux documents.

```cpp
enum class Granularity
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| CharLevel | 0 | Spécifie les modifications au niveau du caractère. |
| WordLevel | 1 | Spécifie les modifications au niveau du mot. |


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

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
