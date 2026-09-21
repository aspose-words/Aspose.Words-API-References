---
title: "Aspose::Words::Comparing::Granularity enum"
linktitle: "Granularity"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comparing::Granularity enum. Anger detaljnivån för förändringar att spåra när två dokument jämförs i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.comparing/granularity/
---
## Granularity enum


Anger detaljnivån för förändringar som ska spåras när två dokument jämförs.

```cpp
enum class Granularity
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| CharLevel | 0 | Anger förändringar på teckennivå. |
| WordLevel | 1 | Anger förändringar på ordnivå. |


## Exempel



Visar hur man specificerar en detaljnivå när man jämför dokument.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Ange om förändringar spåras
// per tecken ('Granularity.CharLevel'), eller per ord ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// Den första dokumentets samling av revisionsgrupper innehåller alla skillnader mellan dokumenten.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## Se även

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
