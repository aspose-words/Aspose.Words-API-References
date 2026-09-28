---
title: "Aspose::Words::Comparing::CompareOptions::get_Granularity метод"
linktitle: "get_Granularity"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Comparing::CompareOptions::get_Granularity метод. Указывает, отслеживаются ли изменения по символу или по слову в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions::get_Granularity method


Указывает, отслеживаются ли изменения по символам или по словам.

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


## Примеры



Показывает, как указать гранулярность при сравнении документов.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Укажите, отслеживаются ли изменения
// по символу ('Granularity.CharLevel'), или по слову ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// Коллекция групп ревизий первого документа содержит все различия между документами.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## См. также

* Enum [Granularity](../../granularity/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
